---
description: 'La tabla ServiceControl se utiliza para controlar los servicios instalados o desinstalados. Nota: los servicios que dependen de la presencia de un ensamblado en la caché de ensamblados global (GAC) no se pueden instalar o iniciar con las tablas ServiceInstall y ServiceControl.'
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Tabla ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815190"
---
# <a name="servicecontrol-table"></a>Tabla ServiceControl

La tabla ServiceControl se utiliza para controlar los servicios instalados o desinstalados.

> [!Note]  
> Los servicios que dependen de la presencia de un [ensamblado](assemblies.md) en la caché de ensamblados global (GAC) no se pueden instalar o iniciar con las tablas [ServiceInstall](serviceinstall-table.md) y ServiceControl. Si necesita iniciar un servicio que depende de un ensamblado en la GAC, debe usar una acción personalizada secuenciada después de la [acción InstallFinalize](installfinalize-action.md) o una [acción personalizada commit](commit-custom-actions.md). Para obtener información sobre cómo instalar ensamblados en la GAC, vea [instalación de ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md).

 

La tabla ServiceControl tiene las columnas siguientes.



| Columna         | Tipo                         | Clave | Nullable |
|----------------|------------------------------|-----|----------|
| ServiceControl | [Identificador](identifier.md) | Y   | N        |
| Nombre           | [Formatea](formatted.md)   | N   | N        |
| Evento          | [Entero](integer.md)       | N   | N        |
| Argumentos      | [Formatea](formatted.md)   | N   | Y        |
| Esperar           | [Entero](integer.md)       | N   | Y        |
| Componente\_    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl
</dt> <dd>

Esta es la clave principal de esta tabla.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Esta columna es la cadena que nombra el servicio. Esta columna se puede usar para controlar un servicio que no está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso
</dt> <dd>

Esta columna contiene las operaciones que se van a realizar en el servicio con nombre. Tenga en cuenta que al detener un servicio, también se detienen todos los servicios que dependen de ese servicio. Al eliminar un servicio que se está ejecutando, el instalador detiene el servicio.

Los valores de este campo son campos de bits que se pueden combinar en un valor único que representa varias operaciones.

Los valores siguientes solo se usan durante la instalación de.



| Constante                           | Hexadecimal | Decimal | Descripción                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventStart**  | 0x001       | 1       | Inicia el servicio durante la [acción StartServices](startservices-action.md).    |
| **msidbServiceControlEventStop**   | 0x002       | 2       | Detiene el servicio durante la [acción StopServices](stopservices-action.md).       |
| (ninguno)                             | 0x004       | 4       | <reserved>                                                                   |
| **msidbServiceControlEventDelete** | 0x008       | 8       | Elimina el servicio durante la [acción DeleteServices](deleteservices-action.md). |



 

Los valores siguientes solo se usan durante la desinstalación.



| Constante                                    | Hexadecimal | Decimal | Descripción                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventUninstallStart**  | 0x010       | 16      | Inicia el servicio durante la [acción StartServices](startservices-action.md).    |
| **msidbServiceControlEventUninstallStop**   | 0x020       | 32      | Detiene el servicio durante la [acción StopServices](stopservices-action.md).       |
| (ninguno)                                      | 0x040       | 64      | <reserved>                                                                   |
| **msidbServiceControlEventUninstallDelete** | 0x080       | 128     | Elimina el servicio durante la [acción DeleteServices](deleteservices-action.md). |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Una lista de argumentos para iniciar los servicios. Los argumentos se separan con caracteres nulos \[ ~ \] . Por ejemplo, la lista de argumentos uno, dos y tres se muestran como: uno \[ ~ \] dos \[ ~ \] tres.

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Currir
</dt> <dd>

Si se sale de este campo null o se especifica un valor de 1, el instalador espera un máximo de 30 segundos para que el servicio se complete antes de continuar. La espera se puede usar para permitir un tiempo adicional para que un evento crítico devuelva un error. Un valor de 0 en este campo significa que solo debe esperar hasta que el administrador de control de servicios (SCM) notifique que este servicio está en estado pendiente antes de continuar con la instalación.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa para la columna uno de la [tabla de componentes](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones [StartServices](startservices-action.md), [StopServices](stopservices-action.md)y [DeleteServices](deleteservices-action.md) en [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

Use la columna nombre para iniciar, detener o eliminar servicios que se van a reemplazar por la instalación o que dependen de un nuevo servicio que se está instalando. Por ejemplo, si escribe el servicio en la columna ServiceControl, puede vincular este servicio a mi componente en la \_ columna componente. Si el campo de bits de la columna de eventos se establece para iniciar mientras se instala, el instalador inicia el servicio al instalar el componente.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



