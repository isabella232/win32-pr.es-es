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
ms.openlocfilehash: dbcf0f90a8bca0cf1f648f74d1b58d7037b79fa8bc9d2d13c4fe2c6dc8306eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996525"
---
# <a name="logfileeventconsumer-class"></a>Clase LogFileEventConsumer

La **clase LogFileEventConsumer** escribe cadenas personalizadas en un archivo de registro de texto cuando se le entregan eventos. Las cadenas están separadas por secuencias de fin de línea. Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener más información, [vea Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

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

La **clase LogFileEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase LogFileEventConsumer** tiene estas propiedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, en función del sistema operativo. Para obtener más información, vea [Enlazar un filtro de eventos con](binding-an-event-filter-with-a-logical-consumer.md) un consumidor lógico y Supervisar y Responder a eventos con [consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Nombre de archivo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de un archivo que incluye la ruta de acceso a la que se anexan las entradas del registro. Si el archivo no existe, **LogFileEventConsumer** intenta crearlo. Se produce un error en el consumidor cuando la ruta de acceso no existe o cuando el usuario que crea el consumidor no tiene permisos de escritura para el archivo o la ruta de acceso.

</dd> <dt>

**IsUnicode**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el archivo de registro es un archivo de texto Unicode. Si **es FALSE,** el archivo de registro es un archivo de texto de código multibyte. Si el archivo existe, esta propiedad se omite y se usa la configuración de archivo actual. Por ejemplo, si **IsUnicode** es **FALSE,** pero el archivo existente es un archivo Unicode, se usa Unicode. Si **IsUnicode** es **TRUE,** pero el archivo es código multibyte, se usa código multibyte.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que Windows Management Instrumentation (WMI) envía eventos.

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**MaximumFileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño máximo de un archivo de registro en bytes. Si el archivo principal supera su tamaño máximo, el contenido se mueve a otro archivo y el archivo principal se vacía. Un valor de 0 (cero) significa que no hay ningún límite de tamaño. El valor predeterminado es 65 535 bytes. El tamaño del archivo se comprueba antes de una operación de escritura. Por lo tanto, puede tener un archivo ligeramente mayor que el límite de tamaño especificado. La siguiente operación de escritura lo detecta e inicia un nuevo archivo.

En la lista siguiente se identifica la estructura de nomenclatura del archivo de copia de seguridad:

-   Si el nombre de archivo original es 8.3, la extensión se reemplaza por una cadena con el formato "001", "002", y así sucesivamente con el número más pequeño mayor que todos los números usados y elegidos anteriormente. Si se usa "999", el número elegido es el número sin usar más pequeño.
-   Si el nombre de archivo original no es 8.3, se anexa al nombre de archivo una cadena con el formato "001", "002", entre otros.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima para un consumidor específico, en bytes.

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

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

Plantilla de [cadena estándar](using-standard-string-templates.md) para el texto de una entrada de registro.

</dd> </dl>

## <a name="remarks"></a>Comentarios

> [!Note]  
> **LogFileEventConsumer** no protege el archivo de registro. Por lo tanto, al configurar **LogFileEventConsumer**, es importante especificar un directorio que esté protegido en el nivel que necesite.

 

La **clase LogFileEventConsumer** se deriva de la [**\_ \_ clase abstracta EventConsumer.**](--eventconsumer.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo del uso **de LogFileEventConsumer** para crear un consumidor, vea Escribir en un archivo de [registro basado en un evento](writing-to-a-log-file-based-on-an-event.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Suscripción \\ raíz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[Creación de un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

