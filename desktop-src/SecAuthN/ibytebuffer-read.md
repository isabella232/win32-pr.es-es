---
description: El método Read lee un número especificado de bytes del objeto de búfer en la memoria a partir del puntero de búsqueda actual.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: Método IByteBuffer::Read (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb78726228e333205032a3179e5c3bedb05786b072d02e78d5cc85cea7a97336
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482675"
---
# <a name="ibytebufferread-method"></a>IByteBuffer::Read (método)

\[El **método Read** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método Read** lee un número especificado de bytes del objeto de búfer en la memoria a partir del puntero de búsqueda actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pByte* \[ out\]
</dt> <dd>

Apunta al búfer en el que se leen los datos del flujo. Si se produce un error, este valor es **NULL.**

</dd> <dt>

*cb* \[ En\]
</dt> <dd>

Número de bytes de datos que se intentan leer del objeto de secuencia.

</dd> <dt>

*readread* \[ out\]
</dt> <dd>

Dirección de una variable **LONG** que recibe el número real de bytes leídos del objeto de secuencia. Puede establecer este puntero en **NULL** para indicar que no está interesado en este valor. En este caso, este método no proporciona el número real de bytes leídos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT**. Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Observaciones

Este método lee bytes de este objeto de secuencia en memoria. El objeto de secuencia debe abrirse en modo \_ STGM READ. Este método ajusta el puntero de búsqueda según el número real de bytes leídos.

El número de bytes leídos realmente también se devuelve en el *parámetro byteRead.*

Notas a los autores de las llamadas

El número real de bytes leídos puede ser menor que el número de bytes solicitado si se produce un error o si se alcanza el final de la secuencia durante la operación de lectura.

Algunas implementaciones pueden devolver un error si se alcanza el final de la secuencia durante la lectura. Debe estar preparado para tratar con los valores devueltos por error o S \_ OK al final de las lecturas de secuencia.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la lectura de bytes del búfer.


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
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



 

