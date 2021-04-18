---
title: Sintaxis
description: Esta es la sintaxis para llamar a FXC.exe, la herramienta de compilador de efectos. Para obtener un ejemplo, vea compilaciones sin conexión.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- FXC, sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105695786"
---
# <a name="syntax"></a>Sintaxis

Esta es la sintaxis para llamar a FXC.exe, la herramienta de compilador de efectos. Para obtener un ejemplo, vea [compilaciones sin conexión](dx-graphics-tools-fxc-using.md).

-   [Uso](#usage)
-   [Argumentos](#arguments)
-   [Comentarios:](#remarks)
-   [Perfiles](#profiles)
-   [Notas de la versión](#version-notes)
-   [Temas relacionados](#related-topics)

## <a name="usage"></a>Uso

*nombres de archivo* de **FXC** *SwitchOptions*

## <a name="arguments"></a>Argumentos
Separe cada opción de modificador con un espacio o dos puntos.

### <a name="switchoptions"></a>*SwitchOptions*
\[en \] Opciones de compilación. Hay solo una opción obligatoria y muchas más que son opcionales. Separe cada uno con un espacio o dos puntos.

#### <a name="required-option"></a>Opción required
##### <a name="t-profile"></a>/T <*perfil*>
Modelo de sombreador (consulte [perfiles](#profiles)).

#### <a name="optional-options"></a>Opciones no necesarias
##### <a name="-help"></a>/?, /help
Ayuda de impresión para `FXC.exe` .

##### <a name="commandoptionfile"></a>@<*comando. Option. File*>
Archivo que contiene opciones de compilación adicionales. Esta opción se puede mezclar con otras opciones de compilación de la línea de comandos. El *comando. Option. File* solo debe contener una opción por línea. El *comando. Option. File* no puede contener ninguna línea en blanco. Las opciones especificadas en el archivo no deben contener espacios iniciales ni finales.

##### <a name="all_resources_bound"></a>/all_resources_bound
Habilite el aplanamiento agresivo en SM 5.1 +. Novedades de Direct3D 12.

##### <a name="cc"></a>/CC
Ensamblado con codificación de color de salida.

##### <a name="compress"></a>/compress
Comprimir el código de bytes del sombreador de contenido DX10 desde archivos.

##### <a name="d-idtext"></a>/D < >=< *texto* de identificador>
Definir macro.

##### <a name="decompress"></a>/decompress
Descomprime el código de bytes del sombreador de contenido DX10 del primer archivo. Los archivos de salida deben aparecer en el orden en que se encontraban durante la compresión.

##### <a name="dumpbin"></a>/dumpbin
Carga un archivo binario en lugar de compilar un sombreador.

##### <a name="e-name"></a>/E <name>
Punto de entrada del sombreador. Si no se proporciona ningún punto de entrada, se considera que **Main** es el nombre de la entrada del sombreador.

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
Habilita las tablas de descriptores sin enlazar. Novedades de Direct3D 12.

##### <a name="extractrootsignature-file"></a>/extractrootsignature <*archivo*>
Extraiga la firma raíz del código de bytes del sombreador. Novedades de Direct3D 12.

##### <a name="fc-file"></a>/FC <*archivo*>
Archivo de lista de código de ensamblado de salida.

##### <a name="fd-file"></a>/FD <*archivo*>
Extraiga la información de la base de datos de programa (PDB) del sombreador y escriba en el archivo especificado. Al compilar el sombreador, utilice/FD para generar un archivo PDB con información de depuración de sombreador.

##### <a name="fe-file"></a>/Fe <*archivo*>
Genera advertencias y errores en el archivo especificado.

##### <a name="fh-file"></a>/FH <*archivo*>
Archivo de encabezado de salida que contiene el código de objeto.

##### <a name="fl-file"></a>/FL <*archivo*
Generar una biblioteca. Requiere el \_47.dll D3dcompiler o una versión posterior del archivo dll.

##### <a name="fo-file"></a>/FO <*archivo*>
Archivo de objeto de salida. A menudo, dada la extensión &quot; . FXC &quot; , aunque se usan otras extensiones, como &quot; . o &quot; , &quot; . obj &quot; o &quot; . dxbc &quot; .

##### <a name="fx-file"></a>/FX ( *archivo* <)>
Código de ensamblado de salida y archivo de lista hexadecimal.

##### <a name="gch"></a>/Gch
Compilar como efecto secundario para los perfiles de fx_4_x.

> [!NOTE]
> La compatibilidad con los perfiles de efectos heredados está en desuso.

##### <a name="gdp"></a>/Gdp
Deshabilitar el modo de rendimiento de efecto.

##### <a name="gec"></a>/Gec
Habilite el modo de compatibilidad con versiones anteriores.

##### <a name="ges"></a>/Ges
Habilita el modo STRICT.

##### <a name="getprivate-file"></a>/getprivate <*archivo*>
Guarde los datos privados del BLOB del sombreador (binario del sombreador compilado) en el archivo especificado. Extrae los datos privados, insertados previamente por/setprivate, del BLOB de sombreador.

Debe especificar la opción/DUMPBIN con/getprivate. Por ejemplo:

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
Evite las construcciones de control de flujo.

##### <a name="gfp"></a>/GFP
Prefiere construcciones de control de flujo.

##### <a name="gis"></a>/Gis
Forzar la limitación IEEE.

##### <a name="gpp"></a>/Gpp
Forzar precisión parcial.
    
##### <a name="i-include"></a>/I <*incluir*>
Ruta de acceso de inclusión adicional.

##### <a name="lx"></a>/Lx
Los literales hexadecimales de salida. Requiere el \_47.dll D3dcompiler o una versión posterior del archivo dll.

##### <a name="matchuavs"></a>/matchUAVs
Coincide con las asignaciones de ranura UAV del sombreador de plantilla en el sombreador actual. Para obtener más información, vea la <a href="#remarks">sección Comentarios</a>.

##### <a name="mergeuavs"></a>/mergeUAVs
Combine las asignaciones de ranura UAV del sombreador de plantilla y del sombreador actual. Para obtener más información, vea la <a href=""></a> <a href="#remarks">sección Comentarios</a>.

##### <a name="ni"></a>/Ni
Números de instrucciones de salida en listas de ensamblados.

##### <a name="no"></a>/No
Desplazamiento de bytes de instrucción de salida en listas de ensamblados. Al generar el ensamblado, utilice/no para anotarlo con el desplazamiento de bytes de cada instrucción.

##### <a name="nologo"></a>/nologo
Se suprime el mensaje de copyright.

##### <a name="od"></a>/Od
Deshabilite las optimizaciones. /OD implica/GFP, aunque la salida no puede ser idéntica a/OD/GFP.

##### <a name="op"></a>/OP
Deshabilitar los sombreadores (en desuso).

##### <a name="o0-o1-o2-o3"></a>/O0/O1,/O2,/O3
Niveles de optimización. O1 es el valor predeterminado.
- O0: deshabilita la reordenación de instrucciones. Esto ayuda a reducir la carga de registro y permite una simulación de bucle más rápida.
- O1: deshabilita la reordenación de instrucciones para ps_3_0 y up.
- O2: igual que O1. Reservado para uso futuro.
- O3: igual que O1. Reservado para uso futuro.

##### <a name="p-file"></a>/P <*archivo*>
Preprocesar para archivo (debe usarse por sí solo).

##### <a name="qstrip_debug"></a>/Qstrip_debug
Quitar datos de depuración del código de bytes del sombreador para perfiles de 4_0 +.

##### <a name="qstrip_priv"></a>/Qstrip_priv
Quite los datos privados del código de bytes de 4_0 + Shader. Quita los datos privados (secuencia arbitraria de bytes) del BLOB del sombreador (binario del sombreador compilado) que se incrustó anteriormente con la `/setprivate <file>` opción.

Debe especificar la opción/DUMPBIN con/Qstrip_priv. Por ejemplo:

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
Quitar datos de reflexión del código de bytes del sombreador para perfiles de 4_0 +.

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
Quitar la firma raíz del código de bytes del sombreador. Novedades de Direct3D 12.

##### <a name="res_may_alias"></a>/res_may_alias
Supongamos que UAVs/SRVs puede tener un alias para cs_5_0 +. Requiere el \_47.dll D3dcompiler o una versión posterior del archivo dll.

##### <a name="setprivate-file"></a>/setprivate <*archivo*>
Agregue los datos privados del archivo especificado al BLOB del sombreador compilado. Inserta el archivo dado, que se trata como un búfer sin formato, en el BLOB del sombreador. Use/setprivate para agregar datos privados al compilar un sombreador. O bien, use la opción/DUMPBIN con/setprivate para cargar un objeto de sombreador existente y, después, después de que el objeto esté en memoria, para agregar el BLOB de datos privados. Por ejemplo, use un solo comando con/setprivate para agregar datos privados a un BLOB de sombreador compilado:

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
O bien, use dos comandos en los que el segundo comando cargue un objeto de sombreador y, a continuación, agregue datos privados:

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>/setrootsignature <*archivo*>
Adjunte la firma raíz al código de bytes del sombreador. Novedades de Direct3D 12.

##### <a name="shtemplate-file"></a>/shtemplate <*archivo*>
Use un archivo de sombreador de plantilla dado para los recursos de combinación (/mergeUAVs) y coincidentes (/matchUAVs). Para obtener más información, vea la <a href="#remarks">sección Comentarios</a>.

##### <a name="vd"></a>/Vd
Deshabilite la validación.

##### <a name="verifyrootsignature-file"></a>/verifyrootsignature <*archivo*>
Compruebe el código de bytes del sombreador con la firma raíz. Novedades de Direct3D 12.

##### <a name="vi"></a>/Vi
Muestra detalles sobre el proceso de inclusión.

##### <a name="vn-name"></a>/VN *nombre* de <>
Use Name como nombre de variable en el archivo de encabezado.

##### <a name="wx"></a>/WX
Trata las advertencias como errores.

##### <a name="zi"></a>/ZI
Habilite la información de depuración.

##### <a name="zpc"></a>/Zpc
Empaquetar matrices en orden principal de columna.

##### <a name="zpr"></a>/Zpr
Empaquetar matrices en orden principal de fila.

### <a name="filenames"></a>*Nombres de archivo*

\[en \] los archivos que contienen los sombreadores y/o los efectos (s).

## <a name="remarks"></a>Observaciones

Use las `/mergeUAVs` `/matchUAVs` Opciones, y `/shtemplate` para alinear las ranuras de enlace UAV para una cadena de sombreadores.

Supongamos que tiene sombreadores A. FX, B. FX y C. FX. Para alinear las ranuras de enlace UAV para esta cadena de sombreadores, se necesitan dos pasos de compilación:

**Para alinear las ranuras de enlace UAV para una cadena de sombreadores**

1.  Use/mergeUAVs para compilar los sombreadores y especifique un BLOB de sombreador compilado previamente con/shtemplate. Por ejemplo:
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  Use/matchUAVs para compilar los sombreadores y especifique el último BLOB del sombreador del primer paso con/shtemplate. Puede compilar en cualquier orden. Por ejemplo:
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
No es necesario volver a compilar C. FX en el segundo paso.

Después de realizar las dos fases anteriores de compilación, puede usar una. o, B. o y C. o como Blobs finales del sombreador con ranuras UAV alineadas.

## <a name="profiles"></a>Profiles

Cada modelo de sombreador se etiqueta con un perfil de HLSL. Para compilar un sombreador en un modelo de sombreador determinado, elija el perfil de sombreador adecuado en la tabla siguiente.

<table><thead><tr class="header"><th>Tipo de sombreador</th><th>Profiles</th></tr></thead><tbody><tr class="odd"><td>Sombreador de cálculo</td><td><dl> cs_4_0<br />
cs_4_1<br />
cs_5_0<br />
cs_5_1<br />
</dl></td></tr><tr class="even"><td>Sombreador de dominios</td><td><dl> ds_5_0<br />
ds_5_1<br />
</dl></td></tr><tr class="odd"><td>Sombreador de geometría</td><td><dl> gs_4_0<br />
gs_4_1<br />
gs_5_0<br />
gs_5_1<br />
</dl></td></tr><tr class="even"><td>Vinculación de sombreador HLSL </td><td><dl> lib_4_0<br />
lib_4_1<br />
lib_4_0_level_9_1<br />
lib_4_0_level_9_1_vs_only<br />
lib_4_0_level_9_1_ps_only<br />
lib_4_0_level_9_3<br />
lib_4_0_level_9_3_vs_only<br />
lib_4_0_level_9_3_ps_only<br />
lib_5_0<br />
</dl> Para obtener más información sobre la vinculación del sombreador, vea <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> y <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>. <br/></td></tr><tr class="odd"><td>Sombreador de casco</td><td><dl> hs_5_0<br />
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

Para Direct3D 12, consulte [especificación de firmas raíz en HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [enlace de recursos en HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) y [indexación dinámica con HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).

En Direct3D 10, use la API para obtener el perfil de vértices, geometría y sombreador de píxeles más adecuado para un dispositivo determinado mediante una llamada a estas funciones: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)y [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).

En Direct3D 9, use los métodos [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) o [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) para recuperar los perfiles de sombreador de vértices y píxeles que admite un dispositivo. La estructura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) devuelta por esos métodos indica el vértice y los perfiles del sombreador de píxeles admitidos por un dispositivo en sus miembros **VertexShaderVersion** y **PixelShaderVersion** .

Para obtener ejemplos, vea [compilar con el compilador actual](dx-graphics-tools-fxc-using.md).

## <a name="related-topics"></a>Temas relacionados

* [Efecto: herramienta de compilador](fxc.md)