---
title: Códigos de retorno de Direct3D 12
description: Los siguientes son códigos de retorno de las funciones de API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359826"
---
# <a name="direct3d-12-return-codes"></a>Códigos de retorno de Direct3D 12

Los siguientes son códigos de retorno de las funciones de API. Para obtener más códigos de retorno, [vea DXGI \_ ERROR](/windows/desktop/direct3ddxgi/dxgi-error).



| HRESULT                                                                  | Descripción                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| NO SE ENCONTRÓ EL ADAPTADOR \_ DE ERROR \_ D3D12 \_ \_                                        | El PSO almacenado en caché especificado se creó en otro adaptador y no se puede reutilizar en el adaptador actual.          |
| D3D12 \_ ERROR \_ DRIVER \_ VERSION \_ MISMATCH                                  | El PSO almacenado en caché especificado se creó en una versión de controlador diferente y no se puede reutilizar en el adaptador actual.  |
| D3DERR \_ INVALIDCALL (reemplazado por DXGI \_ ERROR INVALID \_ \_ CALL)           | La llamada al método no es válida. Por ejemplo, el parámetro de un método puede no ser un puntero válido.                             |
| D3DERR \_ WASSTFUNDDRAWING (reemplazado por DXGI \_ ERROR WAS STILL \_ \_ \_ DRAWING) | La operación blit anterior que transfiere información hacia o desde esta superficie está incompleta.                   |
| E \_ FAIL                                                                  | Se intentó crear un dispositivo con la capa de depuración habilitada y la capa no está instalada.                             |
| E \_ INVALIDARG                                                            | Se pasó un parámetro no válido a la función de devolución.                                                             |
| E \_ OUTOFMEMORY                                                           | Direct3D no pudo asignar memoria suficiente para completar la llamada.                                                   |
| E \_ NOTIMPL                                                               | La llamada al método no se implementa con la combinación de parámetros pasados.                                               |
| S \_ FALSE                                                                 | Valor correcto alternativo, que indica una finalización correcta pero no estándar (el significado preciso depende del contexto). |
| S \_ OK                                                                    | No se ha producido ningún error.                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 