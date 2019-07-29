# code2
package rily.merino.royalmaze;

import net.minecraft.client.renderer.block.model.ModelResourceLocation;
import net.minecraft.creativetab.CreativeTabs;
import net.minecraft.item.Item;
import net.minecraft.util.ResourceLocation;
import net.minecraftforge.client.model.ModelLoader;
import net.minecraftforge.fml.common.Mod;
import net.minecraftforge.fml.common.Mod.EventHandler;
import net.minecraftforge.fml.common.event.FMLPreInitializationEvent;
import net.minecraftforge.fml.common.registry.ForgeRegistries;

@Mod(modid = Sougou.MODID, name = Sougou.MODNAME, version = Sougou.VERSION)
public class Sougou extends Item {
	 public static final String MODID = "moonrosemod";
	 public static final String MODNAME = "MoonroseMod";
	 public static final String VERSION = "1.0";

	 public static Sougou ruby;

 @EventHandler
	 public void preInit(FMLPreInitializationEvent event) {

		 ruby =  (Sougou) new Sougou()
				 .setUnlocalizedName("ruby")
				 .setMaxStackSize(64)
				 .setCreativeTab(CreativeTabs.MISC)
				 .setRegistryName(new ResourceLocation(MODID, "ruby"));

		 ForgeRegistries.ITEMS.register(ruby);

		 ModelLoader.setCustomModelResourceLocation(Sougou.ruby, 0,
				 new ModelResourceLocation(Sougou.ruby.getRegistryName(), "inventory"));

	 }
 }
