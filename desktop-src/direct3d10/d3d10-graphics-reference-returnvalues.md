---
description: La tabla siguiente contiene códigos de retorno de las funciones de API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Códigos de retorno de Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c7e7bca25d240bf7775a6f4d6476148e3749e283ab4f8fb3511bf8b53bb711
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282805"
---
# <a name="direct3d-10-return-codes"></a>Códigos de retorno de Direct3D 10

La tabla siguiente contiene códigos de retorno de las funciones de API.



| HRESULT                                         | Descripción                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| NO SE ENCONTRÓ EL ARCHIVO DE ERROR D3D10 \_ \_ \_ \_                  | No se encontró el archivo.                                                                                                                               |
| ERROR D3D10 \_ \_ DEMASIADOS \_ OBJETOS DE \_ ESTADO \_ \_ ÚNICOS | Hay demasiadas instancias únicas de un tipo determinado de [objeto de estado](d3d10-graphics-programming-guide-api-features-state-objects.md).          |
| D3DERR \_ INVALIDCALL                             | La llamada al método no es válida. Por ejemplo, el parámetro de un método puede no ser un puntero válido.                                                             |
| D3DERR \_ WASSTENGDRAWING                         | La operación de blit anterior que transfiere información hacia o desde esta superficie está incompleta.                                                   |
| E \_ FAIL                                         | Se intentó crear un dispositivo con la capa [de depuración](d3d10-graphics-programming-guide-api-features-layers.md) habilitada y la capa no está instalada. |
| E \_ INVALIDARG                                   | Se pasó un parámetro no válido a la función de devolución.                                                                                            |
| E \_ OUTOFMEMORY                                  | Direct3D no pudo asignar memoria suficiente para completar la llamada.                                                                                   |
| E \_ NOTIMPL                                      | La llamada al método no se implementa con la combinación de parámetros pasados.                                                                              |
| S \_ FALSE                                        | Valor correcto alternativo, que indica una finalización correcta pero no estándar (el significado preciso depende del contexto).                                 |
| S \_ OK                                           | No se ha producido ningún error.                                                                                                                                    |



 

Para escribir código que controle [los valores HRESULT](../winprog/windows-data-types.md) de forma sólida, use las macros SUCCEEDED(hr) y FAILED(hr).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Referencia de Direct3D 10](d3d10-graphics-reference.md)
</dt> </dl>

 

 
