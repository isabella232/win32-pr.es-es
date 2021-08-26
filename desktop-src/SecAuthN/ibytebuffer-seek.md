---
description: El método Seek cambia el puntero de búsqueda a una nueva ubicación relativa al principio del búfer, al final del búfer o al puntero de búsqueda actual.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: Método IByteBuffer::Seek (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 70c4af327fad5014c5d6dec80dd29441f51a03639a108249991c83f53e5d2be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016255"
---
# <a name="ibytebufferseek-method"></a>IByteBuffer::Seek (método)

\[El **método Seek** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método Seek** cambia el puntero de búsqueda a una nueva ubicación relativa al principio del búfer, al final del búfer o al puntero de búsqueda actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dlibMove* \[ En\]
</dt> <dd>

Desplazamiento que se va a agregar a la ubicación indicada por *dwOrigin*. Si *dwOrigin* es STREAM SEEK SET, se interpreta como un valor sin signo en \_ lugar de con \_ signo.

</dd> <dt>

*dwOrigin* \[ En\]
</dt> <dd>

Especifica el origen del desplazamiento especificado en *dlibMove*. El origen puede ser uno de los valores de la tabla siguiente.



| Value                                                                                                                                                                | Significado                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**CONJUNTO \_ DE STREAM SEEK \_**</dt> </dl> | El nuevo puntero de búsqueda es un desplazamiento relativo al principio de la secuencia. En este caso, el *parámetro dlibMove* es la nueva posición de búsqueda relativa al principio de la secuencia.<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**STREAM \_ SEEK \_ CUR**</dt> </dl> | El nuevo puntero de búsqueda es un desplazamiento relativo a la ubicación actual del puntero de búsqueda. En este caso, el *parámetro dlibMove* es el desplazamiento firmado de la posición de búsqueda actual.<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**STREAM \_ SEEK \_ END**</dt> </dl> | El nuevo puntero de búsqueda es un desplazamiento relativo al final de la secuencia. En este caso, el *parámetro dlibMove* es la nueva posición de búsqueda con respecto al final de la secuencia.<br/>             |



 

</dd> <dt>

*plibNewPosition* \[ out\]
</dt> <dd>

Puntero a la ubicación donde este método escribe el valor del nuevo puntero de búsqueda desde el principio de la secuencia. Puede establecer este puntero en **NULL** para indicar que no está interesado en este valor. En este caso, este método no proporciona el nuevo puntero de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT.** Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Comentarios

El **método Seek** cambia el puntero de búsqueda para que las operaciones de lectura y escritura posteriores puedan tener lugar en una ubicación diferente en el objeto de secuencia. Es un error buscar antes del principio de la secuencia. Sin embargo, no es un error buscar más allá del final de la secuencia. Buscar más allá del final de la secuencia es útil para las operaciones de escritura posteriores, ya que la secuencia se extenderá en ese momento a la posición de búsqueda inmediatamente antes de que se haga la operación de escritura.

También puede usar este método para obtener el valor actual del puntero seek llamando a este método con el parámetro *dwOrigin* establecido en STREAM SEEK CUR y el parámetro \_ \_ *dlibMove* establecido en cero para que el puntero seek no cambie. El puntero de búsqueda actual se devuelve en el *parámetro plibNewPosition.*

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo colocar el puntero de búsqueda en una nueva ubicación.


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
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



 

