---
description: Obtiene EL OBJETO IMFDXGIDeviceManager del receptor Microsoft Media Foundation de representación de vídeo.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: MÉTODO IMFDXGIDeviceManagerSource::GetManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474260"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>MÉTODO IMFDXGIDeviceManagerSource::GetManager

Obtiene [**EL OBJETO IMFDXGIDeviceManager del**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) receptor Microsoft Media Foundation de representación de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppManager* \[ out\]
</dt> <dd>

Objeto [**IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFDXGIDeviceManagerSource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




