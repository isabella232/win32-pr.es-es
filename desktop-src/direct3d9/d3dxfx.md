---
description: Opciones para guardar y crear efectos.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995082"
---
# <a name="d3dxfx"></a>D3DXFX

Opciones para guardar y crear efectos.

Las constantes de la tabla siguiente se definen en d3dx9effect.h.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Marcas de guardar y restaurar estado de efecto</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>No se guarda ningún estado al llamar <a href="id3dxeffect--begin.md"><strong>a Begin</strong></a> o restaurar al llamar a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Un bloque de estado guarda el estado al llamar <a href="id3dxeffect--begin.md"><strong>a Begin</strong></a> y restaura el estado al llamar a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Un bloque de estado guarda el estado (excepto los sombreadores y las constantes del sombreador) al llamar a <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> y restaura el estado al llamar a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="odd">
<td>Marcas de creación de efectos</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>El efecto no será clonable y no contendrá ningún dato binario del sombreador. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> no devolverá punteros de función de sombreador. Al establecer esta marca, se reduce el uso de memoria de efecto en aproximadamente un 50 %, ya que elimina la necesidad de que el sistema de efectos mantenga una copia de los sombreadores en memoria. <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect,</strong></a> <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>y <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>usan esta marca.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Habilita la asignación de un recurso de efecto en el espacio de direcciones iniciales de una máquina. Una limitación importante es que no se pueden usar cadenas y identificadores indistintamente. Por ejemplo, lo siguiente ya no funcionaría. <span data-codelanguage=""></span>
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

En su lugar, se debe usar un método como [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) para almacenar el identificador del parámetro , que luego se usa para pasar variables al efecto.</td>
</tr>
</tbody>
</table>



 

Las constantes de la tabla siguiente no están definidas de forma predeterminada y las debe definir el desarrollador.



| Definición del \# preprocesador de efecto | Descripción                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDENTIFICADOR DE \_ DIRECCIÓN GRANDE DE D3DXFX \_   | Defina este valor antes de incluir d3dx9.h para que la aplicación no se compile al intentar pasar cadenas a los parámetros D3DXHANDLE. Esto le ayudará a asegurarse de que se pasa información válida al tiempo de ejecución. |
| Marcas del vinculador de efecto            | Descripción                                                                                                                                                                                                                          |
| CONSCIENTE \_ DE DIRECCIONES \_ GRANDES          | Al establecer la marca de vinculador LARGE ADDRESS AWARE = 1, la aplicación podrá asignar recursos más allá del límite de \_ \_ direcciones de 2 GB cuando sea necesario.                                                                                      |



 

El sistema de efectos usa bloques de estado para guardar y restaurar el estado automáticamente. Para obtener más información sobre los bloques de estado, vea State Blocks Save and Restore State (Direct3D 9) ( Guardar y restaurar estado de bloques de [estado [Direct3D 9]).](state-blocks-save-and-restore-state.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de efecto](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



