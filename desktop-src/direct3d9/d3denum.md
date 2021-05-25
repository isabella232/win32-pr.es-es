---
description: Marca de funcionalidad del controlador.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829d03bf596c24bfb6b3443ace859629f723a664
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343268"
---
# <a name="d3denum"></a>D3DENUM

Marca de funcionalidad del controlador.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Valor</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>Pruebas Laboratorios de calidad de hardware de Windows (WHQL) controladores de Microsoft Laboratorios de calidad de hardware de Windows (WHQL) (WHQL). Se trata de una prueba que consume mucho tiempo y que requiere una penalización de tiempo de un segundo o dos segundos. El miembro WHQLLevel de usa esta <a href="d3dadapter-identifier9.md"><strong>constante D3DADAPTER_IDENTIFIER9</strong></a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> D3DENUM_WHQL_LEVEL está en desuso para Direct3D9Ex que se ejecuta en Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 (o más sistema operativo actual). Cualquiera de estos sistemas operativos devuelve 1 para el nivel WHQL sin comprobar el estado del controlador. <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>Información constante



| Requisito                         | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9.h     |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




