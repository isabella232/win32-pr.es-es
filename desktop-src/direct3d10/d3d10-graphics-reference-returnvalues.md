---
description: La tabla siguiente contiene los códigos de retorno de las funciones de la API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Códigos de retorno de Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686434"
---
# <a name="direct3d-10-return-codes"></a>Códigos de retorno de Direct3D 10

La tabla siguiente contiene los códigos de retorno de las funciones de la API.



| HRESULT                                         | Descripción                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ No \_ se encontró el archivo de error D3D10                  | No se encontró el archivo.                                                                                                                               |
| ERROR de D3D10 \_ \_ demasiados \_ \_ \_ objetos de estado único \_ | Hay demasiadas instancias únicas de un tipo determinado de [objeto de estado](d3d10-graphics-programming-guide-api-features-state-objects.md).          |
| D3DERR \_ INVALIDCALL                             | La llamada al método no es válida. Por ejemplo, el parámetro de un método no puede ser un puntero válido.                                                             |
| D3DERR \_ WASSTILLDRAWING                         | La operación de blit anterior que está transfiriendo información a o desde esta superficie está incompleta.                                                   |
| E \_ FAIL                                         | Se intentó crear un dispositivo con la [capa de depuración](d3d10-graphics-programming-guide-api-features-layers.md) habilitada y la capa no está instalada. |
| E \_ INVALIDARG                                   | Se pasó un parámetro no válido a la función que devuelve.                                                                                            |
| E \_ OUTOFMEMORY                                  | Direct3D no pudo asignar memoria suficiente para completar la llamada.                                                                                   |
| E \_ NOTIMPL                                      | La llamada al método no se implementa con la combinación de parámetros pasada.                                                                              |
| S \_ false                                        | Valor de éxito alternativo, que indica una finalización correcta pero no estándar (el significado exacto depende del contexto).                                 |
| S \_ correcto                                           | No se ha producido ningún error.                                                                                                                                    |



 

Para escribir código que controle [los valores HRESULT](../winprog/windows-data-types.md) sólidamente, use las macros Succeeded (HR) y Failed (HR).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Referencia de Direct3D 10](d3d10-graphics-reference.md)
</dt> </dl>

 

 
