---
description: El método WriteBinary crea un comando de unidad de datos de protocolo de aplicación (APDU) que escribe valores binarios en un archivo elemental.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'ISCardISO7816:: WriteBinary (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000915"
---
# <a name="iscardiso7816writebinary-method"></a>ISCardISO7816:: WriteBinary (método)

\[El método **WriteBinary** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **WriteBinary** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que escribe valores binarios en un archivo elemental.

En función de los atributos de archivo, el comando realiza una de las operaciones siguientes:

-   El OR lógico de los bits que ya están presentes en la tarjeta con los bits especificados en el comando APDU (el estado de borrado lógico de los bits del archivo es 0).
-   El AND lógico de los bits que ya están presentes en la tarjeta con los bits especificados en el comando APDU (el estado de borrado lógico de los bits del archivo es 1).
-   La escritura única en la tarjeta de los bits especificados en el comando APDU.

Cuando no se especifica ninguna indicación en el byte de codificación de datos, se aplica el comportamiento lógico OR.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byP1* \[ de\]
</dt> <dd>

Desplazamiento a la ubicación de escritura desde el principio del archivo binario (EF). Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a escribir en las unidades de datos desde el principio del archivo. Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se va a escribir en las unidades de datos desde el principio del archivo.

</dd> <dt>

*byP2* \[ de\]
</dt> <dd>

Desplazamiento a la ubicación de escritura desde el principio del archivo binario (EF). Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a escribir en las unidades de datos desde el principio del archivo. Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se va a escribir en las unidades de datos desde el principio del archivo.

</dd> <dt>

*pdata* \[ de\]
</dt> <dd>

Puntero a la cadena de unidades de datos que se va a escribir.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está procesando.

Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.

Cuando se ha aplicado una operación de escritura binaria a una unidad de datos de un EF de escritura de una sola vez, cualquier operación de escritura que se refiera a esta unidad de datos se anulará si el contenido de la unidad de datos o el indicador de estado borrado lógico (si existe) asociado a esta unidad de datos es diferente del estado de borrado lógico.

No se puede escribir en los archivos elementales sin una estructura transparente. El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura transparente.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
