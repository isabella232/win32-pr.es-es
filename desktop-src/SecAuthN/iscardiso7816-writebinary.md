---
description: El método WriteBinary construye un comando de unidad de datos de protocolo de aplicación (APDU) que escribe valores binarios en un archivo elemental.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: Método ISCardISO7816::WriteBinary (Scardssp.h)
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
ms.openlocfilehash: 198a8eedc38636f60886af251c8520ef4726f362958c13a25fc3bf32653d7c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922924"
---
# <a name="iscardiso7816writebinary-method"></a>Método ISCardISO7816::WriteBinary

\[El **método WriteBinary** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método WriteBinary** construye un comando [*de*](../secgloss/a-gly.md) unidad de datos de protocolo de aplicación (APDU) que escribe valores binarios en un archivo elemental.

En función de los atributos de archivo, el comando realiza una de las siguientes operaciones:

-   OR lógico de los bits ya presentes en la tarjeta con los bits dados en el comando APDU (el estado borrado lógico de los bits del archivo es 0).
-   AND lógico de los bits ya presentes en la tarjeta con los bits dados en el comando APDU (el estado borrado lógico de los bits del archivo es 1).
-   Escritura única en la tarjeta de los bits dados en el comando APDU.

Cuando no se da ninguna indicación en el byte de codificación de datos, se aplica el comportamiento lógico OR.

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

*byP1* \[ En\]
</dt> <dd>

Desplazamiento a la ubicación de escritura desde el principio del archivo binario (EF). Si b8=1 en P1, b7 y b6 de P1 se establecen en cero (bits RFU), b5 a b1 de P1 son un identificador ef corto y P2 es el desplazamiento del primer byte que se va a escribir en unidades de datos desde el principio del archivo. Si b8=0 en P1, P1 P2 es el desplazamiento del primer byte que se va a escribir en unidades de datos desde el principio \| \| del archivo.

</dd> <dt>

*byP2* \[ En\]
</dt> <dd>

Desplazamiento a la ubicación de escritura desde el principio del archivo binario (EF). Si b8=1 en P1, b7 y b6 de P1 se establecen en cero (bits RFU), b5 a b1 de P1 son un identificador ef corto y P2 es el desplazamiento del primer byte que se va a escribir en unidades de datos desde el principio del archivo. Si b8=0 en P1, P1 P2 es el desplazamiento del primer byte que se va a escribir en unidades de datos desde el principio \| \| del archivo.

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Puntero a la cadena de unidades de datos que se va a escribir.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un [**objeto de interfaz ISCardCmd**](iscardcmd.md) o **NULL.**

Al devolverse, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve a través del *puntero ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Comentarios

El comando encapsulado solo se puede realizar [](../secgloss/s-gly.md) si el estado de seguridad de la tarjeta inteligente satisface los atributos de seguridad del archivo elemental que se está procesando.

Cuando el comando contiene un identificador elemental corto válido, establece el archivo como archivo elemental actual.

Cuando se ha aplicado una operación binaria de escritura a una unidad de datos de una EF de escritura única, cualquier operación de escritura adicional que haga referencia a esta unidad de datos se anulará si el contenido de la unidad de datos o el indicador de estado borrado lógico (si existe) asociado a esta unidad de datos es diferente del estado borrado lógico.

Los archivos elementales sin una estructura transparente no se pueden escribir en . El comando encapsulado anula si se aplica a un archivo elemental sin una estructura transparente.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
