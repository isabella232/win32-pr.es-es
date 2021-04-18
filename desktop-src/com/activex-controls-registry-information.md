---
title: Información del registro de controles ActiveX
description: Información del registro de controles ActiveX
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533525"
---
# <a name="activex-controls-registry-information"></a>Información del registro de controles ActiveX

Hay una serie de entradas y marcas del registro que se usan. Además, los controles pueden admitir categorías de componentes para clasificar las características que proporcionan.

Las claves del registro relacionadas con los controles se marcan con un asterisco en el siguiente árbol:

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

La entrada **DefaultIcon** se usa para identificar un icono que se mostrará cuando el control se minimice a un icono. La función [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) se usa para obtener el icono de. DLL o. Archivo EXE especificado.

La entrada **ToolboxBitmap32** identifica el nombre del módulo y el identificador de recurso para un mapa de bits de 16 \* 15 que se usará para la superficie de una barra de herramientas o un botón del cuadro de herramientas. El tamaño del icono de Windows estándar es demasiado grande para usarse con este fin. Esta entrada admite específicamente los contenedores de controles que tienen un modo de diseño en el que uno selecciona controles y los coloca en un formulario que se está diseñando. Por ejemplo, en Visual Basic, el icono del control se muestra en el cuadro de herramientas Visual Basic durante el modo de diseño.

La entrada de **control** marca un objeto como un control. Los contenedores suelen usar esta entrada para rellenar los cuadros de diálogo. El contenedor usa esta subclave para determinar si se debe incluir un objeto en un cuadro de diálogo que muestre controles.

La subclave **insertable** también se puede usar con controles, dependiendo de si el objeto puede actuar solo como un objeto incrustado en contexto sin características de control especiales. Los objetos marcados con **insertable** aparecen en el cuadro de diálogo Insertar objeto de su contenedor. Normalmente, la entrada **insertable** significa que el control se ha probado con contenedores que no son de control.

Las subclaves **inserciones** y de **control** son opcionales. Un control puede omitir la subclave **insertable** si no está diseñada para trabajar con contenedores más antiguos que no entienden los controles. Un control puede omitir la clave de **control** si solo está diseñada para trabajar con un contenedor específico y, por tanto, no se desea insertar en otros contenedores.

Los controles deben tener un verbo propiedades, OLEIVERB \_ propiedades, junto con cualquier otro verbo que admitan. El verbo de propiedades, así como el verbo estándar OLEIVERB \_ principal, indica al control que muestre su hoja de propiedades. El verbo Properties se muestra como el elemento Properties en el menú del contenedor cuando el control está activo. De este modo, el control puede mostrar su propia página de propiedades, lo que permite una funcionalidad útil para el usuario final, incluso si el contenedor no controla los controles.

Un control define la clave **MiscStatus** para describirse a sí mismo en contenedores potenciales. Los bits toman los valores de [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)y los controles agregan varios valores a esta enumeración. Vea los valores de la enumeración **OLEMISC** para obtener más información. El cliente puede obtener esta información llamando a [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) sin tener que crear una instancia del control en primer lugar.

Por último, la **versión** describe la versión del control que debe coincidir con la versión de la biblioteca de tipos asociada a este control.

También en la información de tipos de un control, el control de atributo marca una entrada de coclase como descripción de un control.

 

 