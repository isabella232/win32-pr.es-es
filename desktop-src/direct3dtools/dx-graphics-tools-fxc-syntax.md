---
title: Syntax
description: Esta es la sintaxis para llamar a FXC.exe, la herramienta del compilador de efectos. Para obtener un ejemplo, vea Compilación sin conexión.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- fxc, sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb39d261b239c44a02ee784f9b8c65483bbe70c1a5e9fbaf5c9c360c8272b2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722412"
---
# <a name="syntax"></a>Syntax

Esta es la sintaxis para llamar a FXC.exe, la herramienta del compilador de efectos. Para obtener un ejemplo, vea [Compilación sin conexión.](dx-graphics-tools-fxc-using.md)

-   [Uso](#usage)
-   [Argumentos](#arguments)
-   [Comentarios:](#remarks)
-   [Perfiles](#profiles)
-   [Notas de la versión](#version-notes)
-   [Temas relacionados](#related-topics)

## <a name="usage"></a>Uso

**fxc** *SwitchOptions* *Filenames*

## <a name="arguments"></a>Argumentos
Separe cada opción de conmutador con un espacio o dos puntos.

### <a name="switchoptions"></a>*SwitchOptions*
\[en \] Opciones de compilación. Solo hay una opción necesaria y muchas más que son opcionales. Separe cada una con un espacio o dos puntos.

#### <a name="required-option"></a>Opción obligatoria
##### <a name="t-profile"></a>Perfil de < /T>
Modelo de sombreador (vea [Perfiles).](#profiles)

#### <a name="optional-options"></a>Opciones no necesarias
##### <a name="-help"></a>/?, /help
Imprimir ayuda para `FXC.exe` .

##### <a name="commandoptionfile"></a>@<*command.option.file*>
Archivo que contiene opciones de compilación adicionales. Esta opción se puede mezclar con otras opciones de compilación de línea de comandos. El *archivo command.option.file* solo debe contener una opción por línea. El *archivo command.option.file* no puede contener ninguna línea en blanco. Las opciones especificadas en el archivo no deben contener espacios iniciales ni finales.

##### <a name="all_resources_bound"></a>/all_resources_bound
Habilite el aplanado agresivo en SM5.1+. Novedad de Direct3D 12.

##### <a name="cc"></a>/Cc
Ensamblado codificado por colores de salida.

##### <a name="compress"></a>/compress
Comprima el código de bytes del sombreador DX10 de los archivos.

##### <a name="d-idtext"></a>Texto del identificador </D >=< >
Definir macro.

##### <a name="decompress"></a>/decompress
Descomprime el código de bytes del sombreador DX10 del primer archivo. Los archivos de salida deben aparecer en el orden en que estaban durante la compresión.

##### <a name="dumpbin"></a>/dumpbin
Carga un archivo binario en lugar de compilar un sombreador.

##### <a name="e-name"></a>/e <name>
Punto de entrada del sombreador. Si no se da ningún punto de entrada, **main** se considera el nombre de la entrada del sombreador.

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
Habilita las tablas de descriptores sin enlazar. Novedad de Direct3D 12.

##### <a name="extractrootsignature-file"></a>/extractrootsignature <*archivo*>
Extraiga la firma raíz del código de bytes del sombreador. Novedad de Direct3D 12.

##### <a name="fc-file"></a>/Fc <*archivo*>
Archivo de lista de código de ensamblado de salida.

##### <a name="fd-file"></a>/Fd <*archivo*>
Extraiga la información de la base de datos del programa de sombreador (PDB) y escriba en el archivo dado. Al compilar el sombreador, use /Fd para generar un archivo PDB con información de depuración del sombreador.

##### <a name="fe-file"></a>Archivo de <*/Fe*>
Genera advertencias y errores en el archivo dado.

##### <a name="fh-file"></a>Archivo de < /Fh>
Archivo de encabezado de salida que contiene código de objeto.

##### <a name="fl-file"></a>/Fl <*archivo*
Generar una biblioteca. Requiere D3dcompiler \_47.dll o una versión posterior del archivo DLL.

##### <a name="fo-file"></a>/Fo <*archivo*>
Archivo de objeto de salida. A menudo se proporciona la extensión .fxc , aunque se usan &quot; &quot; otras extensiones, como &quot; .o , &quot; &quot; .obj &quot; o &quot; .dxbc. &quot;

##### <a name="fx-file"></a>Archivo de <*/Fx*>
Código de ensamblado de salida y archivo de lista hexadecimal.

##### <a name="gch"></a>/Gch
Compile como un efecto secundario para fx_4_x perfiles.

> [!NOTE]
> La compatibilidad con perfiles de efectos heredados está en desuso.

##### <a name="gdp"></a>/Gdp
Deshabilite el modo de rendimiento del efecto.

##### <a name="gec"></a>/Gec
Habilite el modo de compatibilidad con versiones anteriores.

##### <a name="ges"></a>/Ges
Habilite el modo strict.

##### <a name="getprivate-file"></a>/getprivate <*archivo*>
Guarde los datos privados del blob de sombreador (binario de sombreador compilado) en el archivo especificado. Extrae datos privados, previamente insertados por /setprivate, del blob de sombreador.

Debe especificar la opción /dumpbin con /getprivate. Por ejemplo:

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
Evite construcciones de control de flujo.

##### <a name="gfp"></a>/Gfp
Prefiere construcciones de control de flujo.

##### <a name="gis"></a>/Gis
Forzar el estricto ieee.

##### <a name="gpp"></a>/Gpp
Forzar precisión parcial.
    
##### <a name="i-include"></a>/I <*include*>
Ruta de acceso de include adicional.

##### <a name="lx"></a>/Lx
Literales hexadecimales de salida. Requiere D3dcompiler \_47.dll o una versión posterior del archivo DLL.

##### <a name="matchuavs"></a>/matchUAVs
Coincide con las asignaciones de ranuraS de UAV del sombreador de plantillas en el sombreador actual. Para obtener más información, vea <a href="#remarks">Comentarios</a>.

##### <a name="mergeuavs"></a>/mergeUAVs
Combinar asignaciones de ranura de UAV del sombreador de plantillas y el sombreador actual. Para obtener más información, vea <a href=""></a> <a href="#remarks">Comentarios</a>.

##### <a name="ni"></a>/Ni
Números de instrucciones de salida en listas de ensamblados.

##### <a name="no"></a>/No
Desplazamiento de bytes de instrucciones de salida en las listas de ensamblados. Al generar el ensamblado, use /No para anotarlo con el desplazamiento de bytes para cada instrucción.

##### <a name="nologo"></a>/nologo
Se suprime el mensaje de copyright.

##### <a name="od"></a>/Od
Deshabilite las optimizaciones. /Od implica /Gfp, aunque la salida puede no ser idéntica a /Od /Gfp.

##### <a name="op"></a>/Op
Deshabilite los preshaders (en desuso).

##### <a name="o0-o1-o2-o3"></a>/O0 /O1, /O2, /O3
Niveles de optimización. O1 es la configuración predeterminada.
- O0: deshabilita la reordenación de instrucciones. Esto ayuda a reducir la carga del registro y permite una simulación de bucle más rápida.
- O1: deshabilita la reordenación de instrucciones ps_3_0 y hacia arriba.
- O2: igual que O1. Reservado para uso futuro.
- O3: igual que O1. Reservado para uso futuro.

##### <a name="p-file"></a>/P <*archivo*>
Preprocesar en archivo (debe usarse solo).

##### <a name="qstrip_debug"></a>/Qstrip_debug
Quitar datos de depuración del código de bytes del sombreador para perfiles 4_0+.

##### <a name="qstrip_priv"></a>/Qstrip_priv
Quitar los datos privados del código de bytes del sombreador 4_0+. Quita datos privados (secuencia arbitraria de bytes) del blob de sombreador (binario de sombreador compilado) que insertó anteriormente con la `/setprivate <file>` opción .

Debe especificar la opción /dumpbin con /Qstrip_priv. Por ejemplo:

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
Quitar datos de reflexión del código de bytes del sombreador para perfiles 4_0+.

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
Quitar la firma raíz del código de bytes del sombreador. Novedad de Direct3D 12.

##### <a name="res_may_alias"></a>/res_may_alias
Suponga que los UAVs/SRV pueden tener alias para cs_5_0+. Requiere D3dcompiler \_47.dll o una versión posterior del archivo DLL.

##### <a name="setprivate-file"></a>/setprivate <*archivo*>
Agregue datos privados en el archivo especificado al blob de sombreador compilado. Inserta el archivo dado, que se trata como un búfer sin procesar, en el blob del sombreador. Use /setprivate para agregar datos privados al compilar un sombreador. O bien, use la opción /dumpbin con /setprivate para cargar un objeto de sombreador existente y, después, después de que el objeto esté en memoria, para agregar el blob de datos privado. Por ejemplo, use un solo comando con /setprivate para agregar datos privados a un blob de sombreador compilado:

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
O bien, use dos comandos donde el segundo comando carga un objeto de sombreador y, a continuación, agrega datos privados:

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>/setrootsignature <*archivo*>
Adjunte la firma raíz al código de bytes del sombreador. Novedad de Direct3D 12.

##### <a name="shtemplate-file"></a>/shtemplate <*archivo*>
Use un archivo de sombreador de plantillas determinado para combinar (/mergeUAV) y recursos de coincidencia (/matchUAV). Para obtener más información, vea <a href="#remarks">Comentarios</a>.

##### <a name="vd"></a>/Vd
Deshabilite la validación.

##### <a name="verifyrootsignature-file"></a>/verifyrootsignature <*archivo*>
Compruebe el código de bytes del sombreador con la firma raíz. Novedad de Direct3D 12.

##### <a name="vi"></a>/Vi
Muestra detalles sobre el proceso de incluir.

##### <a name="vn-name"></a>/Vn <*nombre*>
Use name como nombre de variable en el archivo de encabezado.

##### <a name="wx"></a>/WX
Trate las advertencias como errores.

##### <a name="zi"></a>/ZI
Habilite la información de depuración.

##### <a name="zpc"></a>/Zpc
Empaquetar matrices en orden de columna principal.

##### <a name="zpr"></a>/Zpr
Empaquetar matrices en orden de fila principal.

### <a name="filenames"></a>*Nombres de archivo*

\[en \] Los archivos que contienen los sombreadores o los efectos.

## <a name="remarks"></a>Comentarios

Use las opciones , y para alinear las ranuras de `/mergeUAVs` enlace `/matchUAVs` `/shtemplate` UAV para una cadena de sombreadores.

Supongamos que tiene sombreadores A.fx, B.fx y C.fx. Para alinear las ranuras de enlace UAV para esta cadena de sombreadores, necesita dos pases de compilación:

**Para alinear las ranuras de enlace UAV para una cadena de sombreadores**

1.  Use /mergeUAV para compilar sombreadores y especifique un blob de sombreador compilado previamente con /shtemplate. Por ejemplo:
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  Use /matchUAV para compilar sombreadores y especifique el último blob de sombreador del primer paso con /shtemplate. Puede compilar en cualquier orden. Por ejemplo:
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
No tiene que volver a compilar C.fx en el segundo paso.

Después de realizar los dos pasos de compilación anteriores, puede usar A.o, B.o y C.o como blobs de sombreador finales con ranuras UAV alineadas.

## <a name="profiles"></a>Profiles

Cada modelo de sombreador se etiqueta con un perfil HLSL. Para compilar un sombreador con un modelo de sombreador determinado, elija el perfil de sombreador adecuado de la tabla siguiente.

<table><thead><tr class="header"><th>Tipo de sombreador</th><th>Profiles</th></tr></thead><tbody><tr class="odd"><td>Sombreador de proceso</td><td><dl> cs_4_0<br />
cs_4_1<br />
cs_5_0<br />
cs_5_1<br />
</dl></td></tr><tr class="even"><td>Sombreador de dominios</td><td><dl> ds_5_0<br />
ds_5_1<br />
</dl></td></tr><tr class="odd"><td>Sombreador de geometría</td><td><dl> gs_4_0<br />
gs_4_1<br />
gs_5_0<br />
gs_5_1<br />
</dl></td></tr><tr class="even"><td>Vinculación del sombreador HLSL </td><td><dl> lib_4_0<br />
lib_4_1<br />
lib_4_0_level_9_1<br />
lib_4_0_level_9_1_vs_only<br />
lib_4_0_level_9_1_ps_only<br />
lib_4_0_level_9_3<br />
lib_4_0_level_9_3_vs_only<br />
lib_4_0_level_9_3_ps_only<br />
lib_5_0<br />
</dl> Para obtener más información sobre la vinculación de sombreador, vea <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> e <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>. <br/></td></tr><tr class="odd"><td>Sombreador de casco</td><td><dl> hs_5_0<br />
hs_5_1<br />
</dl></td></tr><tr class="even"><td>Sombreador de píxeles</td><td><dl> ps_2_0<br />
ps_2_a<br />
ps_2_b<br />
ps_2_sw<br />
ps_3_0<br />
ps_3_sw<br />
ps_4_0<br />
ps_4_0_level_9_0<br />
ps_4_0_level_9_1<br />
ps_4_0_level_9_3<br />
ps_4_1<br />
ps_5_0<br />
ps_5_1<br />
</dl></td></tr><tr class="odd"><td>Firma raíz</td><td><dl> rootsig_1_0<br />
</dl></td></tr><tr class="even"><td>Sombreador de textura</td><td><dl> tx_1_0<br />
</dl></td></tr><tr class="odd"><td>Sombreador de vértices</td><td><dl> vs_1_1<br />
vs_2_0<br />
vs_2_a<br />
vs_2_sw<br />
vs_3_0<br />
vs_3_sw<br />
vs_4_0<br />
vs_4_0_level_9_0<br />
vs_4_0_level_9_1<br />
vs_4_0_level_9_3<br />
vs_4_1<br />
vs_5_0<br />
vs_5_1<br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a>Notas de la versión

Para Direct3D 12, consulte Especificación de firmas raíz en [HLSL,](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl)Enlace de recursos en [HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) e Indexación dinámica mediante [HLSL 5.1.](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1)

En Direct3D 10, use la API para obtener el vértice, la geometría y el perfil de sombreador de píxeles más adecuados para un dispositivo determinado mediante una llamada a estas funciones: [**D3D10GetVertexShaderProfile,**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile) [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)y [**D3D10GetGeometryShaderProfile.**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile)

En Direct3D 9, use los [**métodos GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) o [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) para recuperar los perfiles de sombreador de vértices y píxeles admitidos por un dispositivo. La [**estructura D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) devuelta por esos métodos indica los perfiles de sombreador de vértices y píxeles admitidos por un dispositivo en sus miembros **VertexShaderVersion** y **PixelShaderVersion.**

Para obtener ejemplos, [vea Compilación con el compilador actual.](dx-graphics-tools-fxc-using.md)

## <a name="related-topics"></a>Temas relacionados

* [Herramienta Effect-Compiler](fxc.md)