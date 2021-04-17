---
title: IWMDRMDevice2 GetPartialSyncList, método
description: El método GetPartialSyncList obtiene una lista de sincronización parcial.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Método GetPartialSyncList de Windows Media Administrador de dispositivos
- Método GetPartialSyncList de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice2
- Interfaz IWMDRMDevice2 de Windows Media Administrador de dispositivos, método GetPartialSyncList
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700203"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>IWMDRMDevice2:: GetPartialSyncList (método)

El método **GetPartialSyncList** obtiene una lista de sincronización parcial.

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

*cMinCountThreshold* \[ de\]
</dt> <dd>

Umbral de recuento mínimo.

</dd> <dt>

*cMinHoursThreshold* \[ de\]
</dt> <dd>

Umbral mínimo de horas.

</dd> <dt>

*dwStartingIndex* \[ de\]
</dt> <dd>

Posición inicial de la indización.

</dd> <dt>

*cItems* \[ de\]
</dt> <dd>

Recuento de elementos que se van a indizar.

</dd> <dt>

*ppbSyncList* \[ enuncia\]
</dt> <dd>

Lista de sincronización de licencias recuperada.

</dd> <dt>

*pcbSyncList* \[ enuncia\]
</dt> <dd>

Tamaño de la lista de sincronización de licencias, en bytes.

</dd> <dt>

*pdwNextStartingIndex* \[ enuncia\]
</dt> <dd>

Posición inicial siguiente para la indexación.

</dd> <dt>

*pcItemsProcessed* \[ enuncia\]
</dt> <dd>

Recuento de elementos que se están procesando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Todos los métodos de interfaz de Windows Media Administrador de dispositivos pueden devolver cualquiera de las siguientes clases de códigos de error:

-   Códigos de error COM estándar
-   Códigos de error de Windows convertidos en valores HRESULT
-   Códigos de error de Administrador de dispositivos de Windows Media

Para obtener una lista extensa de posibles códigos de error, consulte [códigos de error](error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMDevice::GetSyncList**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**Interfaz IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





