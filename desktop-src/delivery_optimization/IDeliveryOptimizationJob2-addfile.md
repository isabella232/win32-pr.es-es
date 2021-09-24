---
title: Método AddFile IDeliveryOptimizationJob2
description: El método AddFile agrega un único archivo a un trabajo Optimización de distribución existente.
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
ms.openlocfilehash: 217215d6f4aaf96de8deab37d08cc492392c0631
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128519897"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>Método IDeliveryOptimizationJob2::AddFileWithRanges

El método AddFile agrega un único archivo a un trabajo Optimización de distribución existente.

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

*fileId* \[ En\]
</dt> <dd>

Cadena de identificador de archivo, que identifica de forma única el archivo que se va a descargar.

</dd> <dt>

*remoteUrl* \[ En\]
</dt> <dd>

La dirección URL del Optimización de distribución intentará conectarse para descargar el archivo.

</dd> <dt>

*rangeCount* \[ En\]
</dt> <dd>

Número de elementos contenidos en *los intervalos*. Un valor cero significa que no se usa ningún intervalo para el archivo.

</dd> <dt>

*intervalos* \[ En\]
</dt> <dd>

Lista de intervalos opcional. Cada intervalo de la lista es una [**BG_FILE_RANGE**](bg-file-range.md) estructura.

</dd> <dt>

*riid* \[ En\]
</dt> <dd>

Tipo de objeto contenido en el objeto . Debe ser de tipo IID_IDeliveryOptimizationFile.

</dd> <dt>

*objeto* \[ out\]
</dt> <dd>

Objeto IDeliveryOptimizationFile, que representa el archivo de descarga. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve S_OK correcto o uno de los valores HRESULT estándar en caso de error.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|---------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible  | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]                                  |
| Servidor mínimo compatible  | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]                              |
| Encabezado                    | Deliveryoptimization.h                                                          |
| IDL                       | DeliveryOptimization.idl                                                        |
| Biblioteca                   | Dosvc.lib                                                                       |
| Archivo DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7 |

## <a name="see-also"></a>Consulte también

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
