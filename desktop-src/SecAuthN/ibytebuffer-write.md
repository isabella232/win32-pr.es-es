---
description: El método Write escribe un número especificado de bytes en el objeto de secuencia a partir del puntero de búsqueda actual.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: Método IByteBuffer::Write (Scardssp.h)
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
ms.openlocfilehash: 0033d4f4ee03629d2bedf9f232a43607100bcdca8bfaab457c2236bbfad603d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127355"
---
# <a name="ibytebufferwrite-method"></a>IByteBuffer::Write (método)

\[El **método Write** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método Write** escribe un número especificado de bytes en el objeto de secuencia a partir del puntero de búsqueda actual.

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

*pByte* \[ En\]
</dt> <dd>

Dirección del búfer que contiene los datos que se escribirán en la secuencia. Se debe proporcionar un puntero válido para este parámetro incluso cuando *cb* es cero.

</dd> <dt>

*cb* \[ En\]
</dt> <dd>

Número de bytes de datos que se intentan escribir en la secuencia. Este parámetro puede ser cero.

</dd> <dt>

*cribiendo* \[ out\]
</dt> <dd>

Dirección de una variable **LONG** donde este método escribe el número real de bytes escritos en el objeto de secuencia. El autor de la llamada puede establecer este puntero **en NULL,** en cuyo caso, este método no proporciona el número real de bytes escritos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT**. Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Comentarios

El **método IByteBuffer::Write** escribe los datos especificados en un objeto de secuencia. El puntero de búsqueda se ajusta para el número de bytes escritos realmente. El número de bytes escritos realmente se devuelve en el *parámetro byteWritten.* Si el recuento de bytes es de cero bytes, la operación de escritura no tiene ningún efecto.

Si el puntero de búsqueda está más allá del final de la secuencia y el recuento de bytes es distinto de cero, este método aumenta el tamaño de la secuencia en el puntero de búsqueda y escribe los bytes especificados a partir del puntero de búsqueda. Los bytes de relleno escritos en la secuencia no se inicializan en ningún valor determinado. Esto es lo mismo que el comportamiento de fin de archivo en el sistema de archivos FAT de MS-DOS.

Con un recuento de cero bytes y un puntero de búsqueda más allá del final de la secuencia, este método no crea los bytes de relleno para aumentar la secuencia al puntero de búsqueda. En este caso, debe llamar al método [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) para aumentar el tamaño de la secuencia y escribir los bytes de relleno.

El *parámetro typeWritten* puede tener un valor incluso si se produce un error.

En la implementación proporcionada por COM, los objetos de secuencia no son dispersos. Los bytes de relleno se asignan finalmente en el disco y se asignan a la secuencia.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo escribir bytes en el objeto de secuencia.


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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

