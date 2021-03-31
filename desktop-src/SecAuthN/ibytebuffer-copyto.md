---
description: El método CopyTo copia un número especificado de bytes del puntero de búsqueda actual del objeto en el puntero de búsqueda actual de otro objeto.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'Método IByteBuffer:: CopyTo (Scardssp. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278585"
---
# <a name="ibytebuffercopyto-method"></a>IByteBuffer:: CopyTo (método)

\[El método **CopyTo** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **CopyTo** copia un número especificado de bytes del puntero de búsqueda actual del objeto en el puntero de búsqueda actual de otro objeto.

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

*pByteBuffer* \[ de\]
</dt> <dd>

Apunta a la secuencia de destino. La secuencia a la que apunta *pByteBuffer* puede ser una nueva secuencia o un clon de la secuencia de origen.

</dd> <dt>

*CB* \[ de\]
</dt> <dd>

Número de bytes que se van a copiar desde el flujo de origen.

</dd> <dt>

*pcbRead* \[ enuncia\]
</dt> <dd>

Puntero a la ubicación donde este método escribe el número real de bytes leídos del origen. Puede establecer este puntero en **null** para indicar que no está interesado en este valor. En este caso, este método no proporciona el número real de bytes leídos.

</dd> <dt>

*pcbWritten* \[ enuncia\]
</dt> <dd>

Puntero a la ubicación donde este método escribe el número real de bytes escritos en el destino. Puede establecer este puntero en **null** para indicar que no está interesado en este valor. En este caso, este método no proporciona el número real de bytes escritos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

Este método copia los bytes especificados de una secuencia a otra. También se puede usar para copiar un flujo en sí mismo. El puntero de búsqueda en cada instancia de Stream se ajusta para el número de bytes leídos o escritos.

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



 

