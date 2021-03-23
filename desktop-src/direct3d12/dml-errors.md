---
title: Control de errores y eliminación de dispositivos en DirectML
description: En este tema se describe cómo depurar la eliminación de dispositivos DirectML y otras condiciones de error.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104549116"
---
# <a name="handling-errors-and-device-removal-in-directml"></a>Control de errores y eliminación de dispositivos en DirectML

## <a name="device-removal"></a>Eliminación de dispositivos

Si se produce un error irrecuperable, el dispositivo DirectML puede entrar en el estado "quitado del dispositivo". Los errores irrecuperables que causan la eliminación del dispositivo incluyen el uso no válido de la API (para los métodos que no devuelven un [**valor HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), los errores de controlador, los errores de hardware o las condiciones de memoria insuficiente (OOM).

Cuando se quita un dispositivo DirectML, todas las llamadas a métodos en el dispositivo y todos los objetos creados por ese dispositivo se convierten en no operaciones. En el caso de los métodos que devuelven un [**valor HRESULT**](/windows/desktop/com/structure-of-com-error-codes), se devuelve un código de error [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) . Puede usar el método [ **IDMLDevice:: GetDeviceRemovedReason**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) para comprobar si se ha quitado el dispositivo DirectML y para recuperar un código de error más detallado.

No se puede recuperar de la eliminación del dispositivo, excepto si se libera el dispositivo afectado y todos sus elementos secundarios y, a continuación, se vuelve a crear el dispositivo DirectML desde cero.

La eliminación de dispositivos del dispositivo Direct3D 12 subyacente también hace que se quite el dispositivo DirectML. Sin embargo, esto no es aplicable a la inversa. La eliminación del dispositivo de DirectML puede no hacer que se quite el dispositivo de Direct3D 12 subyacente.

## <a name="debugging-directml-device-removal-and-other-errors"></a>Depuración de dispositivos DirectML: eliminación y otros errores

La causa más común de los errores de DirectML es el uso no válido de la API. El uso de API no válido podría dar lugar a un código de error de **E_INVALIDARG** HRESULT o podría dar lugar a la eliminación del dispositivo.

Se recomienda encarecidamente que habilite la [capa de depuración DirectML](dml-debug-layer.md) durante el desarrollo para detectar y depurar estos errores. La capa de depuración DirectML realiza una validación exhaustiva de los parámetros del método y el uso de la API, y emitirá mensajes de salida de depuración para ayudarle a depurar.

## <a name="see-also"></a>Consulte también

* [Usar la capa de depuración DirectML](dml-debug-layer.md)
