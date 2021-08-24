---
title: Método IDeviceBroker OpenDeviceFromInterfacePath
description: Intenta abrir una instancia de interfaz de dispositivo en nombre de un cliente. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Api de Agente de acceso a dispositivos del método OpenDeviceFromInterfacePath
- Api de Agente de acceso de dispositivos del método OpenDeviceFromInterfacePath, interfaz IDeviceBroker
- IDeviceBroker interface Device Access Broker API , método OpenDeviceFromInterfacePath
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
ms.openlocfilehash: 4d9bd4e03b489a899e182c86207e11ae9ec0fb66cc6c917584d83dcc0aa97918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635335"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>IDeviceBroker::OpenDeviceFromInterfacePath (método)

> [!Important]  
> Estas interfaces no se admiten y no se deben usar. En su lugar, use las API [API de acceso a dispositivos referencia de programación de C++.](device-access-api-c---programming-reference.md)

Intenta abrir una instancia de interfaz de dispositivo en nombre de un cliente. IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszDeviceInterfacePath* \[ En\]
</dt> <dd>

Instancia de interfaz de dispositivo que se abre.

</dd> <dt>

*desiredAccess* \[ En\]
</dt> <dd>

Acceso deseado que se va a pasar para abrirse.

</dd> <dt>

*shareMode* \[ En\]
</dt> <dd>

Modo compartido que se va a pasar para abrirse.

</dd> <dt>

*flagsAndAttributes* \[ En\]
</dt> <dd>

Marcas y atributos que se pasarán para abrirse.

</dd> <dt>

*\* phDevice* \[ out\]
</dt> <dd>

Identificador resultante si la apertura se ha realizado correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve S_OK. De lo contrario, devuelve un código de error de HRESULT.
