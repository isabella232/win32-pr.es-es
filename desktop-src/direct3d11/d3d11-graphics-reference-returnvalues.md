---
title: Códigos de retorno de Direct3D 11
description: Códigos de retorno de las funciones de API.
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d932c3ce3828f375e90bf322af6c42dc112b845f44dfe22f0d0988930129efea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990045"
---
# <a name="direct3d-11-return-codes"></a>Códigos de retorno de Direct3D 11

Códigos de retorno de las funciones de API.

| HRESULT | Descripción |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887C0002) | No se encontró el archivo. |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001) | Hay demasiadas instancias únicas de un tipo determinado de objeto de estado. |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003) | Hay demasiadas instancias únicas de un tipo determinado de objeto de vista. |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004) | La primera llamada a [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) después de [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) o [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) por recurso no se D3D11_MAP_WRITE_DISCARD. |
| D3DERR_INVALIDCALL (se reemplaza por DXGI_ERROR_INVALID_CALL) (0x887A0001) | La llamada al método no es válida. Por ejemplo, el parámetro de un método puede no ser un puntero válido. |
| D3DERR_WASSTILLDRAWING (se reemplaza por DXGI_ERROR_WAS_STILL_DRAWING) (0x887A000A) | La operación blit anterior que transfiere información hacia o desde esta superficie está incompleta. |
| E_FAIL (0x80004005) | Se intentó crear un dispositivo con la capa de depuración habilitada y la capa no está instalada. |
| E_INVALIDARG (0x80070057) | Se pasó un parámetro no válido a la función de devolución. |
| E_OUTOFMEMORY (0x8007000E) | Direct3D no pudo asignar memoria suficiente para completar la llamada. |
| E_NOTIMPL (0x80004001) | La llamada al método no se implementa con la combinación de parámetros pasados. |
| S_FALSE ((HRESULT)1L) | Valor correcto alternativo, que indica una finalización correcta pero no estándar (el significado preciso depende del contexto). |
| S_OK ((HRESULT)0L) | No se ha producido ningún error. |

Para obtener más códigos de retorno, [vea DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).

## <a name="related-topics"></a>Temas relacionados

* [Referencia de Direct3D 11](d3d11-graphics-reference.md)