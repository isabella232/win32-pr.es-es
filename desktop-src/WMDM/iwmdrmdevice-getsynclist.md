---
title: Método IWMDRMDevice GetSyncList
description: El método GetSyncList recupera la lista de sincronización de licencias en el dispositivo. La sincronización de licencias permite al equipo host transferir licencias actualizadas a un dispositivo según los criterios especificados.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Método GetSyncList de Windows Media Administrador de dispositivos
- Método GetSyncList de Windows Media Administrador de dispositivos , interfaz IWMDRMDevice
- Interfaz IWMDRMDevice windows Media Administrador de dispositivos , método GetSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068507"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>IWMDRMDevice::GetSyncList (método)

El **método GetSyncList** recupera la lista de sincronización de licencias en el dispositivo. La sincronización de licencias permite al equipo host transferir licencias actualizadas a un dispositivo según los criterios especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cMinCountThreshold* \[ En\]
</dt> <dd>

Umbral de recuento mínimo.

</dd> <dt>

*cMinHoursThreshold* \[ En\]
</dt> <dd>

Umbral de horas mínimas.

</dd> <dt>

*ppbSyncList* \[ out\]
</dt> <dd>

Se ha recuperado la lista de sincronización de licencias.

</dd> <dt>

*syncSyncList* \[ out\]
</dt> <dd>

Tamaño de la lista de sincronización de licencias, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





