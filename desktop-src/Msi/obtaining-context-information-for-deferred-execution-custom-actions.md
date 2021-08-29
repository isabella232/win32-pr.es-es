---
description: Dado que el script de instalación se puede ejecutar fuera de la sesión de instalación en la que se escribió, es posible que la sesión ya no exista durante la ejecución del script de instalación.
ms.assetid: 13174c5d-c810-4b5d-9d1e-60ed30b8c44d
title: Obtener información de contexto para acciones personalizadas de ejecución aplazada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9016a37eb97c99dc94840617a91ba17da68a0409d6130c15cb17078c60d11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943278"
---
# <a name="obtaining-context-information-for-deferred-execution-custom-actions"></a>Obtener información de contexto para acciones personalizadas de ejecución aplazada

Dado que el script de instalación se puede ejecutar fuera de la sesión de instalación en la que se escribió, es posible que la sesión ya no exista durante la ejecución del script de instalación. En este caso, el identificador de sesión original y las propiedades establecidas durante la secuencia de instalación no están disponibles para una acción personalizada de ejecución aplazada. Las funciones que requieren un identificador de sesión están restringidas a algunos métodos que pueden recuperar información de contexto, o bien las propiedades necesarias durante la ejecución del script deben escribirse en el script de instalación. Por ejemplo, las acciones personalizadas diferidas que llaman a bibliotecas de vínculos dinámicos (DLL) pasan un identificador que solo se puede usar para obtener una cantidad muy limitada de información. Se puede acceder a las funciones que no requieren un identificador de sesión desde una acción personalizada diferida.

Las acciones personalizadas de ejecución aplazada están restringidas a llamar solo a las siguientes funciones que requieren un identificador.



| Función                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)       | Admite un conjunto limitado de propiedades cuando se usa con acciones personalizadas [de](deferred-execution-custom-actions.md)ejecución diferida: la propiedad CustomActionData, la propiedad [**ProductCode**](productcode.md) y [**la propiedad UserSID.**](usersid.md) [Las acciones personalizadas de](commit-custom-actions.md) confirmación no [**pueden usar la función MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obtener la [**propiedad ProductCode.**](productcode.md) Las acciones personalizadas de confirmación pueden usar la propiedad CustomActionData para obtener el código de producto.<br/> |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)     | Admite un conjunto limitado de propiedades cuando se usa con acciones personalizadas de ejecución [diferida:](deferred-execution-custom-actions.md)las propiedades CustomActionData y ProductCode.                                                                                                                                                                                                                                                                                                                                                      |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)               | Cuando se llama desde acciones [](commit-custom-actions.md)personalizadas de ejecución diferida [,](deferred-execution-custom-actions.md)confirmar acciones personalizadas o revertir acciones personalizadas [,](rollback-custom-actions.md) [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) devuelve True o False cuando se solicita para comprobar los parámetros de modo MSIRUNMODE \_ SCHEDULED, MSIRUNMODE COMMIT o \_ MSIRUNMODE \_ ROLLBACK. Las solicitudes para comprobar cualquier otro parámetro de modo de ejecución de una acción personalizada diferida, de confirmación o de reversión devuelven False.<br/>                       |
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)       | Identificador de idioma numérico del producto actual. [Las acciones personalizadas de](commit-custom-actions.md) confirmación no pueden usar la función [**MsiGetLanguage.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) Las acciones personalizadas de confirmación pueden usar la propiedad CustomActionData para obtener el identificador numérico del idioma.<br/>                                                                                                                                                                                                                                                           |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) | Procesa los mensajes de error o progreso de la acción personalizada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Una acción personalizada escrita en JScript o VBScript requiere la instalación del [**objeto Session.**](session-object.md) Es del tipo **Objeto de sesión** y el instalador lo adjunta al script con el nombre "Session". Dado que es posible que el objeto **Session** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en script debe usar uno de los métodos o propiedades siguientes del objeto **Session** para recuperar su contexto.



| Nombre                                                           | Descripción                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Mode (propiedad)**](session-mode.md)                          | Devuelve True solo para MSIRUNMODE \_ SCHEDULED.                                                                                       |
| [**Propiedad Property (objeto Session)**](session-session.md)  | Devuelve la propiedad CustomActionData, [**la propiedad ProductCode**](productcode.md) o [**la propiedad UserSID.**](usersid.md)        |
| [**Propiedad Language (objeto Session)**](session-language.md) | Devuelve el identificador de idioma numérico de la sesión de instalación.                                                                           |
| [**Message (método)**](session-message.md)                      | Se llama para controlar los errores y el progreso.                                                                                              |
| [**Propiedad installer**](session-installer.md)                | Devuelve el objeto primario, que se usa para funciones que no son de sesión, como el acceso al Registro y la administración de configuración del instalador. |



 

Los valores de propiedad que se establecen en el momento en que se procesa la secuencia de instalación en el script pueden no estar disponibles en el momento de la ejecución del script. Solo el siguiente conjunto limitado de propiedades siempre es accesible para las acciones personalizadas durante la ejecución del script.



| Nombre de propiedad                      | Descripción                                                                                                                                                                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Customactiondata                   | La acción personalizada value at time se procesa en la tabla de secuencia. La propiedad CustomActionData solo está disponible para acciones personalizadas de ejecución aplazada. Las acciones personalizadas inmediatas no tienen acceso a esta propiedad. |
| [**ProductCode**](productcode.md) | Código único para el producto, una [cadena GUID.](guid.md)                                                                                                                                                         |
| [**UserSID**](usersid.md)         | Establecido por el instalador en el identificador de seguridad (SID) del usuario.                                                                                                                                                   |



 

Si la acción personalizada de ejecución diferida requiere otros datos de propiedad, sus valores deben almacenarse en el script de instalación. Esto se puede hacer mediante una segunda acción personalizada.

**Para escribir el valor de una propiedad en el script de instalación para su uso durante una acción personalizada de ejecución aplazada**

1.  Inserte una pequeña acción personalizada en la secuencia de instalación que establece la propiedad de interés en una propiedad con el mismo nombre que la acción personalizada de ejecución diferida. Por ejemplo, si la clave principal de la acción personalizada de ejecución diferida es "MyAction", establezca una propiedad denominada "MyAction" en la propiedad X que debe recuperar. Debe establecer la propiedad "MyAction" en la secuencia de instalación antes de la acción personalizada "MyAction". Aunque cualquier tipo de acción personalizada puede establecer los datos de contexto, el método más sencillo es usar una acción personalizada de asignación de propiedades (por ejemplo, Tipo de [acción personalizada 51](custom-action-type-51.md)).
2.  En el momento en que se procesa la secuencia de instalación, el instalador escribirá el valor de la propiedad X en el script de ejecución como el valor de la propiedad CustomActionData.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Referencia de propiedades](property-reference.md)
</dt> </dl>

 

 




