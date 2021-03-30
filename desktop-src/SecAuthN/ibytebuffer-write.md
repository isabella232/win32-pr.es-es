---
description: El método Write escribe un número especificado de bytes en el objeto de flujo, empezando en el puntero de búsqueda actual.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'IByteBuffer:: Write (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912486"
---
# <a name="ibytebufferwrite-method"></a>IByteBuffer:: Write (método)

\[El método de **escritura** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **Write** escribe un número especificado de bytes en el objeto de flujo, empezando en el puntero de búsqueda actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pByte* \[ de\]
</dt> <dd>

Dirección del búfer que contiene los datos que se van a escribir en la secuencia. Se debe proporcionar un puntero válido para este parámetro aunque *CB* sea cero.

</dd> <dt>

*CB* \[ de\]
</dt> <dd>

Número de bytes de datos que se intentan escribir en la secuencia. Este parámetro puede ser cero.

</dd> <dt>

*pcbWritten* \[ enuncia\]
</dt> <dd>

Dirección de una variable **larga** donde este método escribe el número real de bytes escritos en el objeto de secuencia. El autor de la llamada puede establecer este puntero en **null**, en cuyo caso, este método no proporciona el número real de bytes escritos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

El método **IByteBuffer:: Write** escribe los datos especificados en un objeto de secuencia. El puntero de búsqueda se ajusta para el número de bytes escritos realmente. El número de bytes escritos realmente se devuelve en el parámetro *pcbWritten* . Si el recuento de bytes es cero bytes, la operación de escritura no tiene ningún efecto.

Si el puntero de búsqueda está actualmente más allá del final de la secuencia y el recuento de bytes es distinto de cero, este método aumenta el tamaño de la secuencia al puntero de búsqueda y escribe los bytes especificados a partir del puntero de búsqueda. Los bytes de relleno escritos en la secuencia no se inicializan en ningún valor determinado. Esto es lo mismo que el comportamiento de final de archivo en el sistema de archivos FAT de MS-DOS.

Con un recuento de cero bytes y un puntero de búsqueda más allá del final de la secuencia, este método no crea los bytes de relleno para aumentar la secuencia al puntero de búsqueda. En este caso, debe llamar al método [**IByteBuffer:: setSize**](ibytebuffer-setsize.md) para aumentar el tamaño de la secuencia y escribir los bytes de relleno.

El parámetro *pcbWritten* puede tener un valor incluso si se produce un error.

En la implementación proporcionada por COM, los objetos de secuencia no son dispersos. Los bytes de relleno se asignan finalmente en el disco y se asignan a la secuencia.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la escritura de bytes en el objeto de secuencia.


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

