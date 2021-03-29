---
description: Dado que el script de instalación se puede ejecutar fuera de la sesión de instalación en la que se escribió, puede que la sesión ya no exista durante la ejecución del script de instalación.
ms.assetid: 13174c5d-c810-4b5d-9d1e-60ed30b8c44d
title: Obtener información de contexto para las acciones personalizadas de ejecución aplazada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cd956509a5b8a4c92e0a53bfa455154a59bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811287"
---
# <a name="obtaining-context-information-for-deferred-execution-custom-actions"></a>Obtener información de contexto para las acciones personalizadas de ejecución aplazada

Dado que el script de instalación se puede ejecutar fuera de la sesión de instalación en la que se escribió, puede que la sesión ya no exista durante la ejecución del script de instalación. En este caso, el identificador de sesión original y las propiedades que se establecen durante la secuencia de instalación no están disponibles para una acción personalizada de ejecución aplazada. Cualquier función que requiera un identificador de sesión está restringida a algunos métodos que pueden recuperar información de contexto, o bien las propiedades que son necesarias durante la ejecución del script deben escribirse en el script de instalación. Por ejemplo, las acciones personalizadas diferidas que llaman a las bibliotecas de vínculos dinámicos (dll) pasan un identificador que solo se puede usar para obtener una cantidad de información muy limitada. Se puede tener acceso a las funciones que no requieren un identificador de sesión desde una acción personalizada diferida.

Las acciones personalizadas de ejecución aplazada se restringen a llamar solo a las siguientes funciones que requieren un identificador.



| Función                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)       | Admite un conjunto limitado de propiedades cuando se usa con [acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md): la propiedad CustomActionData, la propiedad [**ProductCode**](productcode.md) y la propiedad [**UserSID**](usersid.md) . [Commit Custom Actions](commit-custom-actions.md) no puede usar la función [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obtener la propiedad [**ProductCode**](productcode.md) . Commit Custom Actions puede usar la propiedad CustomActionData para obtener el código de producto.<br/> |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)     | Admite un conjunto limitado de propiedades cuando se usa con [las acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md): las propiedades CustomActionData y ProductCode.                                                                                                                                                                                                                                                                                                                                                      |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)               | Cuando se llama desde acciones personalizadas de [ejecución aplazada](deferred-execution-custom-actions.md), [Confirmar acciones personalizadas](commit-custom-actions.md)o [revertir acciones personalizadas](rollback-custom-actions.md), [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) devuelve true o false cuando se solicita para comprobar los parámetros de modo MSIRUNMODE \_ programado, MSIRUNMODE \_ commit o MSIRUNMODE \_ ROLLBACK. Las solicitudes para comprobar cualquier otro parámetro de modo de ejecución de una acción personalizada aplazada, commit o ROLLBACK devuelven false.<br/>                       |
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)       | IDENTIFICADOR de idioma numérico del producto actual. [Commit Custom Actions](commit-custom-actions.md) no puede usar la función [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) . Commit Custom Actions puede usar la propiedad CustomActionData para obtener el identificador de idioma numérico.<br/>                                                                                                                                                                                                                                                           |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) | Procesa los mensajes de error o de progreso de la acción personalizada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Una acción personalizada escrita en JScript o VBScript requiere el objeto de [**sesión**](session-object.md) de instalación. Este es el objeto de **sesión** de tipo y el instalador lo adjunta al script con el nombre "session". Dado que es posible que el objeto de **sesión** no exista durante la reversión de la instalación, una acción personalizada diferida escrita en el script debe usar uno de los siguientes métodos o propiedades del objeto de **sesión** para recuperar su contexto.



| Nombre                                                           | Descripción                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Propiedad Mode**](session-mode.md)                          | Devuelve true solo para MSIRUNMODE \_ programado.                                                                                       |
| [**Property (propiedad, objeto Session)**](session-session.md)  | Devuelve la propiedad CustomActionData, la propiedad [**ProductCode**](productcode.md) o la propiedad [**UserSID**](usersid.md) .        |
| [**Propiedad Language (objeto Session)**](session-language.md) | Devuelve el identificador de idioma numérico de la sesión de instalación.                                                                           |
| [**Message (método)**](session-message.md)                      | Se llama para controlar los errores y el progreso.                                                                                              |
| [**Propiedad Installer**](session-installer.md)                | Devuelve el objeto primario, que se usa para las funciones que no son de sesión, como el acceso al registro y la administración de la configuración del instalador. |



 

Los valores de propiedad que se establecen en el momento en que se procesa la secuencia de instalación en el script pueden no estar disponibles en el momento de la ejecución del script. Solo el siguiente conjunto limitado de propiedades siempre es accesible para las acciones personalizadas durante la ejecución del script.



| Nombre de propiedad                      | Descripción                                                                                                                                                                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CustomActionData                   | Valor en el momento, la acción personalizada se procesa en la tabla de secuencia. La propiedad CustomActionData solo está disponible para las acciones personalizadas de ejecución aplazada. Las acciones personalizadas inmediatas no tienen acceso a esta propiedad. |
| [**ProductCode**](productcode.md) | Código único del producto, una cadena [GUID](guid.md) .                                                                                                                                                         |
| [**UserSID**](usersid.md)         | Establecido por el instalador en el identificador de seguridad (SID) del usuario.                                                                                                                                                   |



 

Si la acción personalizada de ejecución aplazada requiere otros datos de propiedad, los valores deben almacenarse en el script de instalación. Esto puede hacerse mediante una segunda acción personalizada.

**Para escribir el valor de una propiedad en el script de instalación para su uso durante una acción personalizada de ejecución aplazada**

1.  Inserte una pequeña acción personalizada en la secuencia de instalación que establece la propiedad de interés para una propiedad que tiene el mismo nombre que la acción personalizada de ejecución aplazada. Por ejemplo, si la clave principal de la acción personalizada de ejecución aplazada es "OnAction", establezca una propiedad denominada "OnAction" en la propiedad X que necesita recuperar. Debe establecer la propiedad "OnAction" en la secuencia de instalación antes de la acción personalizada "OnAction". Aunque cualquier tipo de acción personalizada puede establecer los datos de contexto, el método más sencillo consiste en usar una acción personalizada de asignación de propiedades (por ejemplo, el [tipo de acción personalizada 51](custom-action-type-51.md)).
2.  En el momento en que se procesa la secuencia de instalación, el instalador escribe el valor de la propiedad X en el script de ejecución como el valor de la propiedad CustomActionData.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Referencia de propiedades](property-reference.md)
</dt> </dl>

 

 




