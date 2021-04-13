---
title: Método ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice. h)
description: Establece la velocidad de bits almacenada en caché.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- Método SetCachedBitrateMeasurement API de streaming de multimedia
- Método SetCachedBitrateMeasurement API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492868"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>ActiveBasicDevice:: SetCachedBitrateMeasurement (método)

Establece la velocidad de bits almacenada en caché.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*physicalNetworkInterface* \[ de\]
</dt> <dd>

Especifica la interfaz de red física.

</dd> <dt>

*velocidad de bits* \[ de\]
</dt> <dd>

Valor en el que se va a establecer la velocidad de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

