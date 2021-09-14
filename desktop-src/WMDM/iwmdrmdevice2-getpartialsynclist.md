---
title: Método IWMDRMDevice2 GetPartialSyncList
description: El método GetPartialSyncList obtiene una lista de sincronización parcial.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Método GetPartialSyncList de Windows Media Administrador de dispositivos
- Método GetPartialSyncList de Windows Media Administrador de dispositivos interfaz , IWMDRMDevice2
- Interfaz IWMDRMDevice2 windows Media Administrador de dispositivos , método GetPartialSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967816"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>IWMDRMDevice2::GetPartialSyncList (método)

El **método GetPartialSyncList** obtiene una lista de sincronización parcial.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
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

*dwStartingIndex* \[ En\]
</dt> <dd>

Posición inicial para la indexación.

</dd> <dt>

*cItems* \[ En\]
</dt> <dd>

Recuento de elementos que se indexarán.

</dd> <dt>

*ppbSyncList* \[ out\]
</dt> <dd>

Lista de sincronización de licencias recuperadas.

</dd> <dt>

*syncSyncList* \[ out\]
</dt> <dd>

Tamaño de la lista de sincronización de licencias, en bytes.

</dd> <dt>

*pdwNextStartingIndex* \[ out\]
</dt> <dd>

Siguiente posición inicial para la indexación.

</dd> <dt>

*pcItemsProcessed* \[ out\]
</dt> <dd>

Recuento de elementos que se están procesando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Todos los métodos de interfaz de Windows Media Administrador de dispositivos pueden devolver cualquiera de las siguientes clases de códigos de error:

-   Códigos de error COM estándar
-   Windows códigos de error convertidos en valores HRESULT
-   Windows Códigos de error Administrador de dispositivos multimedia

Para obtener una amplia lista de posibles códigos de error, vea [Códigos de error](error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMDevice::GetSyncList**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**IWMDRMDevice2 (interfaz)**](iwmdrmdevice2.md)
</dt> </dl>

 

 





