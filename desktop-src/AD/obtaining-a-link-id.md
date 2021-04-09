---
title: Obtener un identificador de vínculo
description: A partir de Windows Server 2003, ya no es necesario solicitar un linkID de Microsoft; hay un proceso para generar automáticamente un linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Obtener un identificador de vínculo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149173"
---
# <a name="obtaining-a-link-id"></a>Obtener un identificador de vínculo

A partir de Windows Server 2003, ya no es necesario solicitar un [**LinkId**](/windows/desktop/ADSchema/a-linkid) de Microsoft; hay un proceso para generar automáticamente un **LinkId**. El sistema generará automáticamente un identificador de vínculo para un nuevo atributo vinculado cuando el atributo **LinkId** del atributo esté establecido en 1.2.840.113556.1.2.50. Para crear un vínculo de retroceso para este vínculo de avance, establezca el **LinkId** en el [**attributeID**](/windows/desktop/ADSchema/a-attributeid) o [**LDAPDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) del vínculo hacia delante. La caché de esquema debe volver a cargarse después de crear el vínculo hacia delante y antes de crear el vínculo de retroceso. De lo contrario, no se encontrará el **attributeId** o **LDAPDisplayName** del vínculo de reenvío cuando se cree el vínculo de retroceso. La caché de esquema se recarga a petición, unos minutos después de que se realiza un cambio en el esquema o cuando se reinicia el controlador de dominio. Cree todos los vínculos hacia delante, vuelva a cargar la caché de esquema y, a continuación, cree todos los vínculos hacia atrás.

Por ejemplo, si ha creado los nuevos atributos **myForwardLinkAttr** y **myBackLinkAttr**, y desea vincularlos:

> [!Note]  
> Los OID de este ejemplo son inventado. Consulte [obtención de un identificador de objeto de Microsoft](obtaining-an-object-identifier-from-microsoft.md) para obtener instrucciones sobre cómo obtener OID para nuevos atributos.

 

1.  Establezca estos atributos en el atributo que va a ser el vínculo hacia delante:
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  Vuelva a cargar el esquema.
3.  Establezca estos atributos en el atributo que va a ser el vínculo de retroceso:
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos vinculados](linked-attributes.md)
</dt> <dt>

[Cómo extender el esquema](how-to-extend-the-schema.md)
</dt> </dl>

 

 