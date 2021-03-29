---
description: El método commit garantiza que los cambios realizados en un objeto abierto en modo de transacción se reflejan en el almacenamiento principal.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'IByteBuffer:: Commit (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648567"
---
# <a name="ibytebuffercommit-method"></a>IByteBuffer:: Commit (método)

\[El método **commit** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **commit** garantiza que los cambios realizados en un objeto abierto en modo de transacción se reflejan en el almacenamiento principal.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*grfCommitFlags* \[ de\]
</dt> <dd>

Controla la forma en que se confirman los cambios realizados en un objeto de secuencia. Para obtener una definición de estos valores, consulte la enumeración STGC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

Este método garantiza que los cambios en un objeto de secuencia abierto en modo de transacción se reflejan en el almacenamiento primario. Los cambios que se han realizado en la secuencia desde que se abrió o se confirmó por última vez se reflejan en el objeto de almacenamiento primario. Si el elemento primario está abierto en modo de transacción, el elemento primario todavía puede revertir en un momento posterior revirtiendo los cambios en este objeto de flujo. La implementación de archivo compuesto no admite la apertura de secuencias en modo de transacción, por lo que este método tiene muy poco efecto que el vaciado de búferes de memoria.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la confirmación de cambios en el almacenamiento.


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
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



 

