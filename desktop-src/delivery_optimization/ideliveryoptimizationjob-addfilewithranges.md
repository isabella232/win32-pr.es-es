---
title: Método IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization. h)
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
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714645"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>IDeliveryOptimizationJob:: AddFileWithRanges (método)

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

*fileid* \[ de\]
</dt> <dd>

Cadena terminada en null que es un identificador único del contenido publicado. En el caso de contenido no publicado, puede ser cualquier cadena única que el llamador pueda usar para identificar los archivos dentro de un trabajo.

</dd> <dt>

*remoteUrl* \[ de\]
</dt> <dd>

Cadena terminada en null que contiene el nombre del archivo en el servidor.

</dd> <dt>

*localname* \[ de\]
</dt> <dd>

Cadena terminada en null que contiene el nombre del archivo en el cliente.

</dd> <dt>

*rangeCount* \[ en, opcional\]
</dt> <dd>

Número de elementos de *intervalos*.

</dd> <dt>

*intervalos* \[ de en, opcional\]
</dt> <dd>

Matriz de una o varias estructuras de [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) que especifican los intervalos que se van a descargar. No especifique intervalos duplicados o superpuestos.

</dd> <dt>

*archivo* \[ en, opcional\]
</dt> <dd>

Tamaño del archivo en bytes. Pase **DO_UNKNOWN_FILE_SIZE** si la aplicación del llamador no conoce el tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores devueltos, así como otros.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código devuelto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong><strong>S_OK</strong></strong></dt> </dl></td>
<td>Correcto.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>El nombre del archivo local es nulo o es una cadena vacía. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>E_ACCESSDENIED</strong></dt> </dl></td>
<td>El usuario no tiene permiso para escribir en el directorio especificado en el cliente.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_RANGE</strong></dt> </dl></td>
<td>Uno de los intervalos no es válido. Por ejemplo, InitialOffset se establece en <strong>BG_LENGTH_TO_EOF</strong>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </dl></td>
<td>No se pueden especificar intervalos duplicados o superpuestos. <br/>
<blockquote>
[!Note]<br />
Los intervalos se ordenan por el desplazamiento del valor, no por la longitud. Si se especifican intervalos que tienen el mismo desplazamiento, pero están en orden inverso, se devolverá este error. Por ejemplo, si se escriben 100,5 y 100,0 en ese orden, no podrá agregar el archivo al trabajo.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_STATE</strong></dt> </dl></td>
<td>El estado del trabajo no puede ser <strong>BG_JOB_STATE_CANCELLED</strong> o <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

