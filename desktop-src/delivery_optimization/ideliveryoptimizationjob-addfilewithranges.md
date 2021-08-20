---
title: Método IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization.h)
description: Agrega un archivo a un trabajo de descarga y especifica los intervalos del archivo que desea descargar.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Método AddFileWithRanges
- Método AddFileWithRanges, interfaz IDeliveryOptimizationJob
- Interfaz IDeliveryOptimizationJob, método AddFileWithRanges
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 197aa7443123c81d1a675d321b91573823a84f15
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476140"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>IDeliveryOptimizationJob::AddFileWithRanges (método)

Agrega un archivo a un trabajo de descarga y especifica los intervalos del archivo que desea descargar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fileId* \[ En\]
</dt> <dd>

Cadena terminada en NULL que es un identificador único del contenido publicado. Para el contenido no publicado, puede ser cualquier cadena única que el autor de la llamada pueda usar para identificar los archivos dentro de un trabajo.

</dd> <dt>

*remoteUrl* \[ En\]
</dt> <dd>

Cadena terminada en NULL que contiene el nombre del archivo en el servidor.

</dd> <dt>

*localName* \[ En\]
</dt> <dd>

Cadena terminada en NULL que contiene el nombre del archivo en el cliente.

</dd> <dt>

*rangeCount* \[ in, opcional\]
</dt> <dd>

Número de elementos de *ranges.*

</dd> <dt>

*intervalos* \[ in, opcional\]
</dt> <dd>

Matriz de una o [**varias estructuras BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) que especifican los intervalos que se van a descargar. No especifique intervalos duplicados o superpuestos.

</dd> <dt>

*fileSize* \[ in, opcional\]
</dt> <dd>

Tamaño del archivo en bytes. Pase **DO_UNKNOWN_FILE_SIZE** si la aplicación que llama no conoce el tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores devueltos, así como otros.




| Código devuelto | Descripción | 
|-------------|-------------|
| <dl><dt><strong><strong>S_OK</strong></strong></dt></dl> | Correcto.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | El nombre de archivo local es NULL o una cadena vacía. <br /> | 
| <dl><dt><strong>E_ACCESSDENIED</strong></dt></dl> | El usuario no tiene permiso para escribir en el directorio especificado en el cliente.<br /> | 
| <dl><dt><strong>DO_E_INVALID_RANGE</strong></dt></dl> | Uno de los intervalos no es válido. Por ejemplo, InitialOffset se establece <strong>en BG_LENGTH_TO_EOF</strong>.<br /> | 
| <dl><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt></dl> | No puede especificar intervalos duplicados o superpuestos. <br /><blockquote>[!Note]<br />Los intervalos se ordenan por el desplazamiento del valor, no por la longitud. Si se introducen intervalos que tienen el mismo desplazamiento, pero están en orden inverso, se devolverá este error. Por ejemplo, si 100.5 y 100.0 se introducen en ese orden, no podrá agregar el archivo al trabajo.</blockquote><br /> | 
| <dl><dt><strong>DO_E_INVALID_STATE</strong></dt></dl> | El estado del trabajo no se puede <strong>BG_JOB_STATE_CANCELLED</strong> o <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

