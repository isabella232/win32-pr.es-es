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
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160994"
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

El valor devuelto es **un HRESULT**. Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Observaciones

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
| Encabezado<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

