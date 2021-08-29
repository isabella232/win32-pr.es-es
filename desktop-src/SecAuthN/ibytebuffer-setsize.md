---
description: El método SetSize cambia el tamaño del objeto de secuencia.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: Método IByteBuffer::SetSize (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e0d210d7868542bf02b544c91b6f33e3ba6e5381f25462f2cfedce555858cecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016245"
---
# <a name="ibytebuffersetsize-method"></a>IByteBuffer::SetSize (método)

\[El **método SetSize** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método SetSize** cambia el tamaño del objeto de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*libNewSize* \[ En\]
</dt> <dd>

Nuevo tamaño de la secuencia como un número de bytes

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT.** Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Comentarios

El **método IByteBuffer::SetSize** cambia el tamaño del objeto de secuencia. Llame a este método para preasignar el espacio de la secuencia. Si el *parámetro libNewSize* es mayor que el tamaño de secuencia actual, la secuencia se extiende al tamaño indicado rellenando el espacio que interviene con bytes de valor indefinido. Esta operación es similar al [**método IByteBuffer::Write**](ibytebuffer-write.md) si el puntero seek está más allá del final del flujo actual.

Si el *parámetro libNewSize* es menor que la secuencia actual, la secuencia se trunca al tamaño indicado.

El puntero de búsqueda no se ve afectado por el cambio en el tamaño de la secuencia.

Llamar **a IByteBuffer::SetSize** puede ser una manera eficaz de intentar obtener un gran fragmento de espacio contiguo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer el tamaño del búfer.


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
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



 

