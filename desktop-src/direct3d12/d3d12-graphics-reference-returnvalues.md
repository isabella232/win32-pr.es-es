---
title: Códigos de retorno de Direct3D 12
description: A continuación se muestran los códigos de retorno de las funciones de la API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705013"
---
# <a name="direct3d-12-return-codes"></a>Códigos de retorno de Direct3D 12

A continuación se muestran los códigos de retorno de las funciones de la API. Para obtener más códigos de retorno, consulte [ \_ error de DXGI](/windows/desktop/direct3ddxgi/dxgi-error).



| HRESULT                                                                  | Descripción                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ No \_ se encontró el adaptador de error D3D12                                        | El PSO almacenado en caché especificado se creó en un adaptador diferente y no se puede reutilizar en el adaptador actual.          |
| \_Error de \_ coincidencia de versión del controlador de errores D3D12 \_ \_                                  | El PSO almacenado en caché especificado se creó en una versión de controlador diferente y no se puede reutilizar en el adaptador actual.  |
| D3DERR \_ INVALIDCALL (reemplazado por \_ error de DXGI \_ llamada no válida \_ )           | La llamada al método no es válida. Por ejemplo, el parámetro de un método no puede ser un puntero válido.                             |
| D3DERR \_ WASSTILLDRAWING (reemplazado por \_ error de DXGI \_ todavía se está \_ \_ dibujando) | La operación de blit anterior que está transfiriendo información a o desde esta superficie está incompleta.                   |
| E \_ FAIL                                                                  | Se intentó crear un dispositivo con la capa de depuración habilitada y la capa no está instalada.                             |
| E \_ INVALIDARG                                                            | Se pasó un parámetro no válido a la función que devuelve.                                                             |
| E \_ OUTOFMEMORY                                                           | Direct3D no pudo asignar memoria suficiente para completar la llamada.                                                   |
| E \_ NOTIMPL                                                               | La llamada al método no se implementa con la combinación de parámetros pasada.                                               |
| S \_ false                                                                 | Valor de éxito alternativo, que indica una finalización correcta pero no estándar (el significado exacto depende del contexto). |
| S \_ correcto                                                                    | No se ha producido ningún error.                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 