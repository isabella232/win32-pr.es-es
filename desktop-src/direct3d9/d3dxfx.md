---
description: Opciones para guardar y crear efectos.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1e5e57b5fac94c1fb24d35cf1826057b75c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151958"
---
# <a name="d3dxfx"></a>D3DXFX

Opciones para guardar y crear efectos.

Las constantes de la tabla siguiente se definen en d3dx9effect. h.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Estado del efecto guardar y restaurar marcas</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>No se guarda ningún Estado cuando se llama a <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> o restore cuando se llama a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Un stateblock guarda el estado al llamar a <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> y restaura el estado al llamar a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Un stateblock guarda el estado (excepto los sombreadores y las constantes del sombreador) al llamar a <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> y restaura el estado cuando se llama a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="odd">
<td>Marcas de creación de efectos</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>El efecto será no clonable y no contendrá ningún dato binario de sombreador. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> no devolverá punteros de función de sombreador. La configuración de esta marca reduce el uso de memoria de efecto en aproximadamente el 50% porque elimina la necesidad de que el sistema de efectos mantenga una copia de los sombreadores en la memoria. Esta marca se usa en <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>y <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Habilita la asignación de un recurso de efecto en el espacio de direcciones de uppder de un equipo. Una limitación importante es que no se pueden usar cadenas y administrar indistintamente. Por ejemplo, lo siguiente dejará de funcionar. <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

En su lugar, se debe usar un método como [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) para almacenar el identificador del parámetro, que se usa para pasar variables al efecto.</td>
</tr>
</tbody>
</table>



 

Las constantes de la tabla siguiente no se definen de forma predeterminada y las debe definir el desarrollador.



|                                |                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Definición del preprocesador \# de efectos | Descripción                                                                                                                                                                                                                          |
| D3DXFX \_ identificador de LARGEADDRESS \_   | Defina este valor antes de incluir d3dx9. h para que la aplicación no pueda compilarse al intentar pasar cadenas a los parámetros de D3DXHANDLE. Esto le ayudará a asegurarse de que se pasa información válida al tiempo de ejecución. |
| Efectos del enlazador de efectos            | Descripción                                                                                                                                                                                                                          |
| \_reconocimiento de direcciones grandes \_          | Si se establece la marca del enlazador \_ , la dirección grande \_ consciente = 1 permitirá a la aplicación asignar recursos más allá del límite de 2 GB de direcciones cuando sea necesario.                                                                                      |



 

El sistema de efectos usa bloques de estado para guardar y restaurar el estado automáticamente. Para obtener más información sobre los bloques de estado, vea estado de guardado y restauración del estado de los [bloques de estado (Direct3D 9)](state-blocks-save-and-restore-state.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de efecto](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



