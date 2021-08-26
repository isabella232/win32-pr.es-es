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
ms.openlocfilehash: 9e42e42e88dfa2acec9061a54f3a8fcc96128ad5aee6ff004e49f6dd10062074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957844"
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
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFDXGIDeviceManagerSource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




