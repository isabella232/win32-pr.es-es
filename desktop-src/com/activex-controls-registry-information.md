---
title: ActiveX Controla la información del Registro
description: ActiveX Controla la información del Registro
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264631"
---
# <a name="activex-controls-registry-information"></a>ActiveX Controla la información del Registro

Hay una serie de entradas y marcas del Registro que se usan. Además, los controles pueden admitir categorías de componentes para clasificar las características que proporcionan.

Las claves del Registro relacionadas con los controles se marcan con un asterisco en el árbol siguiente:

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

La **entrada DefaultIcon** se usa para identificar un icono que se mostrará cuando el control se minimice a un icono. La [**función ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) se usa para obtener el icono del .DLL o .EXE especificado.

La **entrada ToolboxBitmap32** identifica el nombre del módulo y el identificador de recursos de un mapa de bits de 16 15 que se usará para la cara de un botón de barra de herramientas \* o cuadro de herramientas. El tamaño Windows icono estándar es demasiado grande para usarse para este propósito. Esta entrada admite específicamente contenedores de controles que tienen un modo de diseño en el que se seleccionan los controles y se coloca en un formulario que se está diseñando. Por ejemplo, en Visual Basic, el icono del control se muestra en el cuadro de herramientas Visual Basic durante el modo de diseño.

La **entrada Control** marca un objeto como un control . A menudo, los contenedores usan esta entrada para rellenar cuadros de diálogo. El contenedor usa esta subclave para determinar si se debe incluir un objeto en un cuadro de diálogo que muestra controles.

La **subclave Insertable** también se puede usar con controles, en función de si el objeto solo puede actuar como un objeto incrustado en posición sin características de control especiales. Los objetos **marcados con Insertable** aparecen en el cuadro de diálogo Insertar objeto de su contenedor. La **entrada Insertable** generalmente significa que el control se ha probado con contenedores que no son de control.

Las **subclave Insertable** y **Control** son opcionales. Un control puede omitir la subclave **Insertable** si no está diseñado para funcionar con contenedores anteriores que no entiendan los controles. Un control puede omitir la **clave control** si solo está diseñado para funcionar con un contenedor específico y, por tanto, no desea insertarse en otros contenedores.

Los controles deben tener un verbo Propiedades, OLEIVERB PROPERTIES, junto con cualquier \_ otro verbo que admitan. El verbo Properties, así como el verbo estándar OLEIVERB PRIMARY, indica \_ al control que muestre su hoja de propiedades. El verbo Propiedades se muestra como el elemento Propiedades en el menú del contenedor cuando el control está activo. De este modo, el control puede mostrar su propia página de propiedades, lo que permite alguna funcionalidad útil al usuario final, incluso si el contenedor no controla los controles.

Un control define la **clave MiscStatus** para describirse a sí mismo en contenedores potenciales. Los bits toman los valores de [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)y los controles agregan varios valores a esta enumeración. Vea los **valores de enumeración OLEMISC** para obtener más información. El cliente puede obtener esta información llamando a [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) sin tener que crear primero una instancia del control.

Por último, **Versión** describe la versión del control que debe coincidir con la versión de la biblioteca de tipos asociada a este control.

También en la información de tipo de un control, el control de atributo marca una entrada de la clase coclase como que describe un control.

 

 