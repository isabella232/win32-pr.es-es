---
description: El método Read Lee un número especificado de bytes del objeto de búfer en la memoria a partir del puntero de búsqueda actual.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'IByteBuffer:: Read (método) (Scardssp. h)'
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
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278580"
---
# <a name="ibytebufferread-method"></a>IByteBuffer:: Read (método)

\[El método **Read** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **Read** Lee un número especificado de bytes del objeto de búfer en la memoria a partir del puntero de búsqueda actual.

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

*pByte* \[ enuncia\]
</dt> <dd>

Apunta al búfer en el que se leen los datos de la secuencia. Si se produce un error, este valor es **null**.

</dd> <dt>

*CB* \[ de\]
</dt> <dd>

Número de bytes de datos que se intentan leer del objeto de secuencia.

</dd> <dt>

*pcbRead* \[ enuncia\]
</dt> <dd>

Dirección de una variable **larga** que recibe el número real de bytes leídos del objeto de secuencia. Puede establecer este puntero en **null** para indicar que no está interesado en este valor. En este caso, este método no proporciona el número real de bytes leídos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

Este método lee los bytes de este objeto de secuencia en la memoria. El objeto de secuencia debe estar abierto en el \_ modo de lectura STGM. Este método ajusta el puntero de búsqueda por el número real de bytes leídos.

El número de bytes realmente leídos también se devuelve en el parámetro *pcbRead* .

Notas a los autores de las llamadas

El número real de bytes leídos puede ser menor que el número de bytes solicitado si se produce un error o si se alcanza el final de la secuencia durante la operación de lectura.

Es posible que algunas implementaciones devuelvan un error si se alcanza el final de la secuencia durante la lectura. Debe estar preparado para tratar con los valores devueltos de error devueltos o \_ de aceptar al final de las lecturas de flujo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo leer bytes del búfer.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

