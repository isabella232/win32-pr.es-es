---
description: El método ReadBinary crea un comando de unidad de datos de protocolo de aplicación (APDU) que adquiere un mensaje de respuesta que proporciona la parte del contenido de un archivo elemental estructurado de forma transparente.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'ISCardISO7816:: ReadBinary (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912465"
---
# <a name="iscardiso7816readbinary-method"></a>ISCardISO7816:: ReadBinary (método)

\[El método **ReadBinary** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ReadBinary** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que adquiere un mensaje de respuesta que proporciona la parte del contenido de un archivo elemental estructurado de forma transparente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byP1* \[ de\]
</dt> <dd>

El campo P1-P2, desplazado hasta el primer byte que se va a leer desde el principio del archivo. Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a leer en las unidades de datos desde el principio del archivo. Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se leerá en unidades de datos desde el principio del archivo.

</dd> <dt>

*byP2* \[ de\]
</dt> <dd>

El campo P1-P2, desplazado hasta el primer byte que se va a leer desde el principio del archivo. Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a leer en las unidades de datos desde el principio del archivo. Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se leerá en unidades de datos desde el principio del archivo.

</dd> <dt>

*lBytesToRead* \[ de\]
</dt> <dd>

Número de bytes que se van a leer del EF transparente.

Si el campo le contiene solo ceros, dentro del límite de 256 para la longitud corta o 65536 para la longitud extendida, se deben leer todos los bytes hasta el final del archivo.

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

Los archivos elementales sin una estructura transparente no se pueden borrar. El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura transparente.

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

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
