---
description: El método Seek cambia el puntero de búsqueda a una nueva ubicación con respecto al principio del búfer, al final del búfer o al puntero de búsqueda actual.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'IByteBuffer:: Seek (método) (Scardssp. h)'
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
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912489"
---
# <a name="ibytebufferseek-method"></a>IByteBuffer:: Seek (método)

\[El método **Seek** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **Seek** cambia el puntero de búsqueda a una nueva ubicación con respecto al principio del búfer, al final del búfer o al puntero de búsqueda actual.

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

*dlibMove* \[ de\]
</dt> <dd>

Desplazamiento que se va a agregar a la ubicación indicada por *dwOrigin*. Si *dwOrigin* es \_ el conjunto de búsqueda de secuencias \_ , se interpreta como un valor sin signo en lugar de con signo.

</dd> <dt>

*dwOrigin* \[ de\]
</dt> <dd>

Especifica el origen del desplazamiento especificado en *dlibMove*. El origen puede ser uno de los valores de la tabla siguiente.



| Value                                                                                                                                                                | Significado                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**\_conjunto de búsqueda de secuencias \_**</dt> </dl> | El nuevo puntero de búsqueda es un desplazamiento relativo al principio de la secuencia. En este caso, el parámetro *dlibMove* es la nueva posición de búsqueda en relación con el principio de la secuencia.<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**STREAM \_ Seek \_ CUR**</dt> </dl> | El nuevo puntero de búsqueda es un desplazamiento relativo a la ubicación del puntero de búsqueda actual. En este caso, el parámetro *dlibMove* es el desplazamiento con signo de la posición de búsqueda actual.<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**\_final de búsqueda de flujo \_**</dt> </dl> | El nuevo puntero de búsqueda es un desplazamiento relativo al final de la secuencia. En este caso, el parámetro *dlibMove* es la nueva posición de búsqueda en relación con el final de la secuencia.<br/>             |



 

</dd> <dt>

*plibNewPosition* \[ enuncia\]
</dt> <dd>

Puntero a la ubicación donde este método escribe el valor del nuevo puntero de búsqueda desde el principio de la secuencia. Puede establecer este puntero en **null** para indicar que no está interesado en este valor. En este caso, este método no proporciona el nuevo puntero de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

El método de **búsqueda** cambia el puntero de búsqueda, por lo que las operaciones de lectura y escritura posteriores pueden tener lugar en una ubicación diferente en el objeto de secuencia. Es un error buscar antes del principio de la secuencia. No obstante, no se trata de un error para buscar más allá del final de la secuencia. Buscar más allá del final de la secuencia es útil para las operaciones de escritura posteriores, ya que la secuencia en ese momento se extenderá a la posición de búsqueda inmediatamente antes de que se realice la operación de escritura.

También puede usar este método para obtener el valor actual del puntero de búsqueda llamando a este método con el parámetro *dwOrigin* establecido en Stream \_ Seek \_ CUR y el parámetro *dlibMove* establecido en cero para que no se cambie el puntero de búsqueda. El puntero de búsqueda actual se devuelve en el parámetro *plibNewPosition* .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo colocar el puntero de búsqueda a una nueva ubicación.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

