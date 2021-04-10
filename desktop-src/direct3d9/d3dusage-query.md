---
description: Estas opciones identifican los tipos de recursos de consulta.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153126"
---
# <a name="d3dusage_query"></a>\_Consulta D3DUSAGE

Estas opciones identifican los tipos de recursos de consulta.



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                                   | Descripción                                                                                                                                                                                                                                                                                                                                         |
| \_Filtro de consulta D3DUSAGE \_                    | Consulte el formato de recursos para ver si admite tipos de filtro de textura distintos \_ del punto D3DTEXF (que siempre se admite).                                                                                                                                                                                                                         |
| \_LEGACYBUMPMAP consulta \_ D3DUSAGE             | Consultar el recurso sobre un mapa de rugosidad heredado.                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ consulta \_ POSTPIXELSHADER \_ blending | Consulte el recurso para comprobar la compatibilidad con la compatibilidad con la fusión de sombreador de píxeles post. Si [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) produce un error con D3DUSAGE \_ query \_ POSTPIXELSHADER \_ blending, no se admiten las operaciones de combinación de píxeles post. Entre ellas se incluyen la prueba alfa, la niebla de píxeles, la mezcla de destino de representación, la habilitación de escritura de color y la interpolación. |
| \_SRGBREAD consulta \_ D3DUSAGE                  | Consulte el recurso para comprobar si una textura admite la corrección gamma durante una operación de lectura.                                                                                                                                                                                                                                                        |
| \_SRGBWRITE consulta \_ D3DUSAGE                 | Consulte el recurso para comprobar si una textura admite la corrección gamma durante una operación de escritura.                                                                                                                                                                                                                                                       |
| \_VERTEXTEXTURE consulta \_ D3DUSAGE             | Consulte el recurso para comprobar la compatibilidad con el muestreo de textura del sombreador de vértices.                                                                                                                                                                                                                                                                            |
| \_WRAPANDMIP consulta \_ D3DUSAGE                | Consulte el recurso para comprobar la compatibilidad con el ajuste de textura y la asignación de MIP.                                                                                                                                                                                                                                                                          |



 

Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) para consultar la compatibilidad de hardware para estos usos y otros usos que se enumeran en [D3DUSAGE](d3dusage.md).

## <a name="constant-information"></a>Información constante



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3d9types. h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
