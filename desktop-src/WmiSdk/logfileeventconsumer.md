---
description: La clase LogFileEventConsumer escribe cadenas personalizadas en un archivo de registro de texto cuando se le entregan eventos.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Clase LogFileEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696920"
---
# <a name="logfileeventconsumer-class"></a>Clase LogFileEventConsumer

La clase **LogFileEventConsumer** escribe cadenas personalizadas en un archivo de registro de texto cuando se le entregan eventos. Las cadenas se separan mediante secuencias de final de línea. Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a>Miembros

La clase **LogFileEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **LogFileEventConsumer** tiene estas propiedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, dependiendo del sistema operativo. Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nombre de archivo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de un archivo que incluye la ruta de acceso a la que se anexan las entradas de registro. Si el archivo no existe, **LogFileEventConsumer** intenta crearlo. Se produce un error en el consumidor cuando la ruta de acceso no existe o cuando el usuario que crea el consumidor no tiene permisos de escritura para el archivo o la ruta de acceso.

</dd> <dt>

**IsUnicode**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, el archivo de registro es un archivo de texto Unicode. Si es **false**, el archivo de registro es un archivo de texto de código multibyte. Si el archivo existe, se omite esta propiedad y se usa la configuración del archivo actual. Por ejemplo, si **IsUnicode** es **false**, pero el archivo existente es un archivo Unicode, se usa Unicode. Si **IsUnicode** es **true**, pero el archivo es código multibyte, se utiliza código multibyte.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumFileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño máximo de un archivo de registro en bytes. Si el archivo principal supera su tamaño máximo, el contenido se mueve a un archivo diferente y se vacía el archivo principal. Un valor de 0 (cero) significa que no hay límite de tamaño. El valor predeterminado es 65.535 bytes. El tamaño del archivo se comprueba antes de una operación de escritura. Por lo tanto, puede tener un archivo que sea ligeramente mayor que el límite de tamaño especificado. La siguiente operación de escritura lo detecta e inicia un nuevo archivo.

En la siguiente lista se identifica la estructura de nomenclatura del archivo de copia de seguridad:

-   Si el nombre de archivo original es 8,3, la extensión se sustituye por una cadena con el formato "001", "002", y así sucesivamente por el número más pequeño mayor que todos los números elegidos y usados anteriormente. Si se usa "999", el número elegido es el número más pequeño que no se usa.
-   Si el nombre de archivo original no es 8,3, se anexa al nombre de archivo una cadena con el formato "001", "002", etc.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima para un consumidor específico, en bytes.

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](key-qualifier.md)
</dt> </dl>

Nombre único para este consumidor.

</dd> <dt>

**Texto**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

[Plantilla](using-standard-string-templates.md) de cadena estándar para el texto de una entrada de registro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> **LogFileEventConsumer** no protege el archivo de registro. Por lo tanto, cuando configure **LogFileEventConsumer**, es importante especificar un directorio que esté protegido con el nivel que necesite.

 

La clase **LogFileEventConsumer** se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo del uso de **LogFileEventConsumer** para crear un consumidor, consulte [escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\Suscripción raíz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[Crear un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

