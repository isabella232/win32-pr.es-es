---
description: Construye un comando de unidad de datos de protocolo de aplicación (APDU) que establece secuencialmente parte del contenido de un archivo básico en su estado borrado lógico, empezando por un desplazamiento determinado.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: Método ISCardISO7816::EraseBinary (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 012927e21e3ed897136a9b058ae03539b7d2e2ac0e581d04cb14235aed9ae80f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007903"
---
# <a name="iscardiso7816erasebinary-method"></a>Método ISCardISO7816::EraseBinary

\[El **método EraseBinary** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método EraseBinary** construye un comando de unidad de datos de protocolo de aplicación (APDU) que establece secuencialmente parte del contenido de un archivo básico en su estado borrado lógico, empezando por un desplazamiento determinado. [](../secgloss/a-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byP1* \[ En\]
</dt> <dd>

Posición de RFU.

Si b8=1 en P1, b7 y b6 de P1 se establecen en cero (bits RFU), b5 a b1 de P1 son un identificador ef corto y P2 es el desplazamiento del primer byte que se va a borrar (en unidades de datos) desde el principio del archivo.

Si b8=0 en P1, P1 P2 es el desplazamiento del primer byte que se va a borrar (en unidades de datos) desde el principio \| \| del archivo.

Si el campo de datos está presente, codifica el desplazamiento de la primera unidad de datos que no se va a borrar. Este desplazamiento debe ser mayor que el codificado en P1-P2. Cuando el campo de datos está vacío, el comando se borra hasta el final del archivo.

</dd> <dt>

*byP2* \[ En\]
</dt> <dd>

Posición de RFU.

Si b8=1 en P1, b7 y b6 de P1 se establecen en cero (bits RFU), b5 a b1 de P1 son un identificador ef corto y P2 es el desplazamiento del primer byte que se va a borrar (en unidades de datos) desde el principio del archivo.

Si b8=0 en P1, P1 P2 es el desplazamiento del primer byte que se va a borrar (en unidades de datos) desde el principio \| \| del archivo.

Si el campo de datos está presente, codifica el desplazamiento de la primera unidad de datos que no se va a borrar. Este desplazamiento debe ser mayor que el codificado en P1-P2. Cuando el campo de datos está vacío, el comando se borra hasta el final del archivo.

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Puntero a los datos que especifica el intervalo de borrado. Este parámetro puede ser **NULL.**

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **NULL.**

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve mediante el *puntero ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La operación se ha completado correctamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se pasó un parámetro que no es válido.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>              |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                            |



 

## <a name="remarks"></a>Comentarios

El comando encapsulado solo se puede realizar [](../secgloss/s-gly.md) si el estado de seguridad de la tarjeta inteligente satisface los atributos de seguridad del archivo básico que se está procesando.

Cuando el comando contiene un identificador básico corto válido, establece el archivo como archivo básico actual.

Los archivos elementales sin una estructura transparente no se pueden borrar. El comando encapsulado anula si se aplica a un archivo básico sin una estructura transparente.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
