---
title: Enlace en tiempo de ejecución en el capó
description: En este tema se describe cómo funciona el enlace en tiempo de ejecución en ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, enlace en tiempo de ejecución, lo que sucede en el capó
- enlazar AD, enlace en tiempo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488275"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Enlace en tiempo de ejecución: ¿Qué está ocurriendo en el capó?

En la siguiente lista se describe el proceso general para realizar un enlace en tiempo de ejecución:

-   Algo enlaza a un objeto de directorio ADSI. Por ejemplo, "LDAP: Fiera = Juanpérez, OU = sales, DC = Fabrikam, DC = COM" enlaza mediante enlace COM en tiempo de ejecución. Esto hace que ADSI llame al método [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en la interfaz **IDispatch** .
-   ADSI busca un objeto en la clase User y crea un objeto que admite las interfaces adecuadas, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   ADSI realiza una búsqueda en el registro y busca CLSID de extensión para el usuario. Tenga en cuenta que ADSI almacena en caché estos datos.
-   Algo realiza una llamada al método **MyNewMethod** . ADSI busca su identificador de envío y los ID. de envío de otras extensiones ADSI. ADSI busca la extensión que sirve a esta llamada y llama a la interfaz [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para esa extensión.
-   La extensión ejecuta la función.
-   Ahora, el escritor de cliente invoca el método **YourNewMethod** con la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para la extensión actual. La implementación de **IDispatch** de la extensión delega en **IDispatch** para ADSI.
-   La interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para ADSI vuelve a buscar la extensión adecuada, o a continuación, llama a la extensión adecuada mediante la interfaz [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para esa extensión.

 

 