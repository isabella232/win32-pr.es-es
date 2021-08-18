---
title: Obtención de un identificador de vínculo
description: A partir Windows Server 2003, ya no es necesario solicitar un linkID a Microsoft; hay un proceso para generar automáticamente un linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Obtención de un identificador de vínculo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1800448e8cc665e0a28a88800a592e33d7b6ee5a766743d8a681a121c5ad02c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025563"
---
# <a name="obtaining-a-link-id"></a>Obtención de un identificador de vínculo

A partir Windows Server 2003, ya no es necesario solicitar un [**linkID**](/windows/desktop/ADSchema/a-linkid) a Microsoft; hay un proceso para generar automáticamente un **linkID**. El sistema generará automáticamente un identificador de vínculo para un nuevo atributo vinculado cuando el atributo **linkID** del atributo esté establecido en 1.2.840.113556.1.2.50. Para crear un vínculo hacia atrás para este vínculo hacia delante, se establece **linkID** en [**attributeID**](/windows/desktop/ADSchema/a-attributeid) o [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) del vínculo hacia delante. La memoria caché de esquema debe volver a cargarse después de crear el vínculo hacia delante y antes de crear el vínculo de reserva. De lo contrario, el **atributo attributeId** o **ldapDisplayName** del vínculo hacia delante no se encontrará cuando se cree el vínculo atrás. La memoria caché de esquema se vuelve a cargar a petición, unos minutos después de realizar un cambio de esquema o cuando se reinicia el controlador de dominio. Cree todos los vínculos hacia delante, vuelva a cargar la caché de esquemas y, a continuación, cree todos los vínculos de reserva.

Por ejemplo, cuando haya creado los nuevos atributos **myForwardLinkAttr** y **myBackLinkAttr** y desee vincularlos:

> [!Note]  
> Los OD de este ejemplo se derivan. Consulte [Obtención de un identificador de objeto de Microsoft para](obtaining-an-object-identifier-from-microsoft.md) obtener instrucciones sobre cómo obtener ID para nuevos atributos.

 

1.  Establezca estos atributos en el atributo que va a ser el vínculo hacia delante:
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  Vuelva a cargar el esquema.
3.  Establezca estos atributos en el atributo que va a ser el vínculo atrás:
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos vinculados](linked-attributes.md)
</dt> <dt>

[Extensión del esquema](how-to-extend-the-schema.md)
</dt> </dl>

 

 