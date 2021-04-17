---
description: Obtiene el IMFDXGIDeviceManager del receptor de representación de vídeo Microsoft Media Foundation.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'IMFDXGIDeviceManagerSource:: GetManager (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697025"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>IMFDXGIDeviceManagerSource:: GetManager (método)

Obtiene el [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) del receptor de representación de vídeo Microsoft Media Foundation.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppManager* \[ enuncia\]
</dt> <dd>

El objeto [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFDXGIDeviceManagerSource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




