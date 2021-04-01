---
title: IDeliveryOptimizationJob2 AddFile (método)
description: El método AddFile agrega un solo archivo a un trabajo existente.
keywords:
- AddFile (método)
- Método AddFile, interfaz IDeliveryOptimizationJob2
- Interfaz IDeliveryOptimizationJob2, método AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150076"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>IDeliveryOptimizationJob2:: AddFileWithRanges (método)

El método AddFile agrega un solo archivo a un trabajo existente.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*fileid* \[ de\]
</dt> <dd>

Cadena de identificador de archivo que identifica de forma única el archivo que se va a descargar.

</dd> <dt>

*remoteUrl* \[ de\]
</dt> <dd>

La dirección URL del archivo que intentará conectarse para descargar el archivo.

</dd> <dt>

*rangeCount* \[ de\]
</dt> <dd>

Número de elementos contenidos en *rangos*. Un valor cero significa que no se utiliza ningún intervalo para el archivo.

</dd> <dt>

*intervalos* \[ de de\]
</dt> <dd>

La lista de intervalos opcional. Cada intervalo de la lista es una estructura de [**BG_FILE_RANGE**](bg-file-range.md) .

</dd> <dt>

*riid* \[ de\]
</dt> <dd>

El tipo de objeto contenido en el objeto. Debe ser de tipo IID_IDeliveryOptimizationFile.

</dd> <dt>

*objeto* \[ de enuncia\]
</dt> <dd>

El objeto IDeliveryOptimizationFile, que representa el archivo de descarga. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve S_OK si se realiza correctamente o uno de los valores HRESULT estándar en caso de error.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|---------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible  | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]                                  |
| Servidor mínimo compatible  | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]                              |
| Encabezado                    | Deliveryoptimization. h                                                          |
| IDL                       | DeliveryOptimization. idl                                                        |
| Biblioteca                   | Dosvc. lib                                                                       |
| Archivo DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7 |

## <a name="see-also"></a>Vea también

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
