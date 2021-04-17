---
title: Propiedad CmClassGuid de IMsRdpDeviceV2
description: Contiene el GUID de la clase de instalación de Configuration Manager para el dispositivo.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad CmClassGuid
- Propiedad CmClassGuid Servicios de Escritorio remoto, interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, propiedad CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676557"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>IMsRdpDeviceV2:: CmClassGuid (propiedad)

Contiene el GUID de la clase de instalación de Configuration Manager para el dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>Valor de propiedad

GUID de la clase de instalación de Configuration Manager para el dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 con SP1<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2 con SP1<br/>                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





