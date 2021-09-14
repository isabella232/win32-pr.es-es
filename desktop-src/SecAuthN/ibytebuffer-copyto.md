---
description: El método CopyTo copia un número especificado de bytes del puntero de búsqueda actual del objeto al puntero de búsqueda actual de otro objeto.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: Método IByteBuffer::CopyTo (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244371"
---
# <a name="ibytebuffercopyto-method"></a>IByteBuffer::CopyTo (método)

\[El **método CopyTo** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método CopyTo** copia un número especificado de bytes del puntero de búsqueda actual del objeto al puntero de búsqueda actual de otro objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pByteBuffer* \[ En\]
</dt> <dd>

Apunta al flujo de destino. La secuencia a la que *apunta pByteBuffer* puede ser una nueva secuencia o un clon de la secuencia de origen.

</dd> <dt>

*cb* \[ En\]
</dt> <dd>

Número de bytes que se copian de la secuencia de origen.

</dd> <dt>

*readread* \[ out\]
</dt> <dd>

Puntero a la ubicación donde este método escribe el número real de bytes leídos del origen. Puede establecer este puntero en **NULL** para indicar que no está interesado en este valor. En este caso, este método no proporciona el número real de bytes leídos.

</dd> <dt>

*yescribe* \[ out\]
</dt> <dd>

Puntero a la ubicación donde este método escribe el número real de bytes escritos en el destino. Puede establecer este puntero en **NULL** para indicar que no está interesado en este valor. En este caso, este método no proporciona el número real de bytes escritos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT.** Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Observaciones

Este método copia los bytes especificados de una secuencia a otra. También se puede usar para copiar una secuencia en sí misma. El puntero de búsqueda de cada instancia de secuencia se ajusta para el número de bytes leídos o escritos.

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



 

