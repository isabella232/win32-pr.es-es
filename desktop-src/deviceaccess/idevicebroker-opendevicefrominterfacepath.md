---
title: IDeviceBroker OpenDeviceFromInterfacePath, método
description: Intenta abrir una instancia de la interfaz de dispositivo en nombre de un cliente. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Método OpenDeviceFromInterfacePath API de agente de acceso a dispositivos
- Método OpenDeviceFromInterfacePath API de agente de acceso a dispositivos, interfaz IDeviceBroker
- Interfaz IDeviceBroker API de agente de acceso de dispositivos, método OpenDeviceFromInterfacePath
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420211"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>IDeviceBroker:: OpenDeviceFromInterfacePath (método)

> [!Important]  
> Estas interfaces no se admiten y no se deben usar. En su lugar, use las API de la referencia de programación de C++ de la [API de acceso a dispositivos](device-access-api-c---programming-reference.md) .

Intenta abrir una instancia de la interfaz de dispositivo en nombre de un cliente. IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszDeviceInterfacePath* \[ de\]
</dt> <dd>

Instancia de la interfaz de dispositivo que se va a abrir.

</dd> <dt>

*desiredAccess* \[ de\]
</dt> <dd>

Acceso deseado que se va a pasar a Open.

</dd> <dt>

*shareMode* \[ de\]
</dt> <dd>

Modo de uso compartido que se pasará a Open.

</dd> <dt>

*flagsAndAttributes* \[ de\]
</dt> <dd>

Marcas y atributos que se van a pasar a Open.

</dd> <dt>

*\* phDevice* \[\]
</dt> <dd>

Identificador resultante si se ha abierto correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, Devuelve S_OK. De lo contrario, devuelve un código de error HRESULT.
