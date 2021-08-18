---
description: La tabla ServiceControl se usa para controlar los servicios instalados o desinstalados. Nota Los servicios que se basan en la presencia de un ensamblado en la caché global de ensamblados (GAC) no se pueden instalar ni iniciar mediante las tablas ServiceInstall y ServiceControl.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Tabla ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b8531fb70c1887d77ae9b09bf3fe7e59de0c7878dfac44707df942e838f4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039985"
---
# <a name="servicecontrol-table"></a>Tabla ServiceControl

La tabla ServiceControl se usa para controlar los servicios instalados o desinstalados.

> [!Note]  
> Los servicios que se [](assemblies.md) basan en la presencia de un ensamblado en la caché global de ensamblados (GAC) no se pueden instalar ni iniciar mediante las [tablas ServiceInstall](serviceinstall-table.md) y ServiceControl. Si necesita iniciar un servicio que depende de un ensamblado en la GAC, debe usar una acción personalizada secuenciada después de la acción [InstallFinalize](installfinalize-action.md) o una acción personalizada [de confirmación](commit-custom-actions.md). Para obtener información sobre cómo instalar ensamblados en la GAC, vea [Instalación de ensamblados en la caché global de ensamblados.](installation-of-assemblies-to-the-global-assembly-cache.md)

 

La tabla ServiceControl tiene las siguientes columnas.



| Columna         | Tipo                         | Clave | Nullable |
|----------------|------------------------------|-----|----------|
| ServiceControl | [Identificador](identifier.md) | Y   | N        |
| Nombre           | [Formato](formatted.md)   | N   | N        |
| Evento          | [Entero](integer.md)       | N   | N        |
| Argumentos      | [Formato](formatted.md)   | N   | Y        |
| Esperar           | [Entero](integer.md)       | N   | Y        |
| Componente\_    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl
</dt> <dd>

Esta es la clave principal de esta tabla.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Esta columna es la cadena que asigna nombre al servicio. Esta columna se puede usar para controlar un servicio que no está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Esta columna contiene las operaciones que se realizarán en el servicio con nombre. Tenga en cuenta que al detener un servicio, también se detienen todos los servicios que dependen de ese servicio. Al eliminar un servicio que se está ejecutando, el instalador detiene el servicio.

Los valores de este campo son campos de bits que se pueden combinar en un único valor que representa varias operaciones.

Los valores siguientes solo se usan durante una instalación.



| Constante                           | Hexadecimal | Decimal | Descripción                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventStart**  | 0x001       | 1       | Inicia el servicio durante la [acción StartServices](startservices-action.md).    |
| **msidbServiceControlEventStop**   | 0x002       | 2       | Detiene el servicio durante la [acción StopServices](stopservices-action.md).       |
| (ninguno)                             | 0x004       | 4       | <reserved>                                                                   |
| **msidbServiceControlEventDelete** | 0x008       | 8       | Elimina el servicio durante la acción [DeleteServices](deleteservices-action.md). |



 

Los valores siguientes solo se usan durante una desinstalación.



| Constante                                    | Hexadecimal | Decimal | Descripción                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventUninstallStart**  | 0x010       | 16      | Inicia el servicio durante la [acción StartServices](startservices-action.md).    |
| **msidbServiceControlEventUninstallStop**   | 0x020       | 32      | Detiene el servicio durante la [acción StopServices](stopservices-action.md).       |
| (ninguno)                                      | 0x040       | 64      | <reserved>                                                                   |
| **msidbServiceControlEventUninstallDelete** | 0x080       | 128     | Elimina el servicio durante la acción [DeleteServices](deleteservices-action.md). |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Lista de argumentos para iniciar servicios. Los argumentos están separados por caracteres NULL \[ ~ \] . Por ejemplo, la lista de argumentos One, Two y Three se muestra como: One \[ ~ \] Two \[ ~ \] Three.

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Esperar
</dt> <dd>

Si se deja este campo como null o se especifica un valor de 1, el instalador espera un máximo de 30 segundos para que el servicio se complete antes de continuar. La espera se puede usar para permitir un tiempo adicional para que un evento crítico devuelva un error. Un valor de 0 en este campo significa esperar solo hasta que el administrador de control de servicios (SCM) informe de que este servicio está en un estado pendiente antes de continuar con la instalación.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa a la columna uno de la [tabla de componentes](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las [acciones StartServices,](startservices-action.md) [StopServices](stopservices-action.md)y [DeleteServices](deleteservices-action.md) de las tablas de secuencia [*procesan*](s-gly.md) la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

Use la columna Nombre para iniciar, detener o eliminar servicios que se están reemplazando por la instalación o que dependen de un nuevo servicio que se está instalando. Por ejemplo, escribir MyService en la columna ServiceControl puede vincular este servicio a MyComponent en la columna \_ Component . Si el campo de bits de la columna Evento está establecido para iniciarse durante la instalación, el instalador inicia MyService al instalar MyComponent.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



