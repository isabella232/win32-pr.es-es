---
title: Cómo integra ADSI Extensions
description: Instrucciones que describen cómo interactúa ADSI con las extensiones.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- ADSI de extensiones
- ADSI y extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078365"
---
# <a name="how-adsi-integrates-extensions"></a>Cómo integra ADSI Extensions

Las instrucciones siguientes describen cómo interactúa ADSI con las extensiones:

-   Algo enlaza a un objeto de directorio ADSI. Por ejemplo, "LDAP:Rio = Juanpérez, OU = sales, DC = Fabrikam, DC = COM".
-   ADSI identifica que el objeto está en la clase de **usuario** .
-   ADSI realiza una búsqueda en el registro e identifica los CLSID de la extensión para el **usuario**. Tenga en cuenta que ADSI almacena en caché estos datos.
-   Algo llama al método **QueryInterface** para IID \_ IMyExtension. ADSI busca las interfaces asociadas al objeto de **usuario** , comenzando por sus propias interfaces y, a continuación, examinando las interfaces de extensión.
-   Si se encuentra una coincidencia, ADSI crea una instancia del componente que admite IID \_ IMyExtension y llama a **QueryInterface** para la extensión. Se devuelve la interfaz resultante.
-   El usuario usa esta interfaz para llamar a los métodos de interfaz.
-   A continuación, el cliente llama a **QueryInterface** para IID \_ IYourExtension, que se encuentra en un componente diferente. Este componente delega esta llamada **QueryInterface** en la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del agregador, que resulta ser ADSI propiamente dicha.
-   De nuevo, ADSI busca las interfaces y crea la instancia de componente.

 

 