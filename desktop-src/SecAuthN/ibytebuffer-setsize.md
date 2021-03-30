---
description: El método setSize cambia el tamaño del objeto de secuencia.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'IByteBuffer:: setSize (método) (Scardssp. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002758"
---
# <a name="ibytebuffersetsize-method"></a>IByteBuffer:: setSize (método)

\[El método **setSize** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **setSize** cambia el tamaño del objeto de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*libNewSize* \[ de\]
</dt> <dd>

Nuevo tamaño de la secuencia como un número de bytes

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

El método **IByteBuffer:: setSize** cambia el tamaño del objeto de secuencia. Llame a este método para asignar previamente espacio para la secuencia. Si el parámetro *libNewSize* es mayor que el tamaño de la secuencia actual, el flujo se extiende hasta el tamaño indicado rellenando el espacio intermedio con bytes de valor sin definir. Esta operación es similar al método [**IByteBuffer:: Write**](ibytebuffer-write.md) si el puntero de búsqueda está más allá del final actual de la secuencia.

Si el parámetro *libNewSize* es menor que el flujo actual, el flujo se trunca al tamaño indicado.

El puntero de búsqueda no se ve afectado por el cambio en el tamaño de la secuencia.

Llamar a **IByteBuffer:: setSize** puede ser una manera eficaz de intentar obtener un gran fragmento de espacio contiguo.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

