---
title: IWMDRMDevice GetSyncList, método
description: El método GetSyncList recupera la lista de sincronización de licencias en el dispositivo. La sincronización de licencias permite al equipo host transferir licencias actualizadas a un dispositivo de acuerdo con los criterios especificados.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Método GetSyncList de Windows Media Administrador de dispositivos
- Método GetSyncList de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método GetSyncList
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699615"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>IWMDRMDevice:: GetSyncList (método)

El método **GetSyncList** recupera la lista de sincronización de licencias en el dispositivo. La sincronización de licencias permite al equipo host transferir licencias actualizadas a un dispositivo de acuerdo con los criterios especificados.

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

*cMinCountThreshold* \[ de\]
</dt> <dd>

Umbral de recuento mínimo.

</dd> <dt>

*cMinHoursThreshold* \[ de\]
</dt> <dd>

Umbral mínimo de horas.

</dd> <dt>

*ppbSyncList* \[ enuncia\]
</dt> <dd>

Lista de sincronización de licencias recuperada.

</dd> <dt>

*pcbSyncList* \[ enuncia\]
</dt> <dd>

Tamaño de la lista de sincronización de licencias, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





