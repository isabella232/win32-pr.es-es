---
title: Implementar el objeto COM de extensión de creación de objetos
description: Una extensión de creación de objetos es un objeto COM implementado como un servidor en proceso. Tanto las extensiones de creación de objetos principales como las secundarias deben implementar la interfaz IDsAdminNewObjExt.
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- Implementar la extensión de creación de objetos AD de objeto COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c1a9da94caa300c1277cf6f6030357ca9d573d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077511"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>Implementar el objeto COM de extensión de creación de objetos

Una extensión de creación de objetos es un objeto COM implementado como un servidor en proceso. Tanto las extensiones de creación de objetos principales como las secundarias deben implementar la interfaz [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) .

## <a name="implementing-idsadminnewobjext"></a>Implementación de IDsAdminNewObjExt

Cuando se crea el Asistente para creación de objetos, inicializa cada extensión de creación de objetos llamando al método [**IDsAdminNewObjExt:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) de la extensión. El método **Initialize** proporciona la extensión con información sobre el contenedor en el que se crea el objeto, el nombre de clase del nuevo objeto e información sobre el propio asistente. Si se inicia el Asistente para creación de objetos con el fin de crear un nuevo objeto a partir de un objeto existente, el parámetro *pADsCopySource* no será **null**. En este caso, la extensión debe intentar obtener tantos datos del objeto que se va a copiar como sea factible.

Una vez inicializada la extensión, se llama al método [**IDsAdminNewObjExt:: AddPages**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) . La extensión debe agregar la página o páginas al asistente durante este método. Una página del asistente se crea rellenando una estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) y pasando después esta estructura a la función [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . A continuación, la página se agrega al asistente mediante una llamada a la función de devolución de llamada que se pasa a **AddPages** en el parámetro *lpfnAddPage* .

Antes de que se muestre la página de la extensión, se llama a [**IDsAdminNewObjExt:: SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) . Esto proporciona la extensión con un puntero de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) para el objeto que se va a crear.

Mientras se muestra la página del asistente, la página debe controlar y responder a los mensajes de notificación necesarios del asistente, como [**PSN \_ SETACTIVE**](../controls/psn-setactive.md) y [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md).

Cuando el usuario completa todas las páginas del asistente, el asistente mostrará una página "finalizar" que proporciona un resumen de los datos especificados. El asistente obtiene estos datos llamando al método [**IDsAdminNewObjExt:: GetSummaryInfo**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) para cada una de las extensiones. El método **GetSummaryInfo** proporciona un **BSTR** que contiene los datos de texto que se muestran en la página "finalizar". Una extensión de creación de objetos no tiene que proporcionar datos de resumen. En este caso, **GetSummaryInfo** debe devolver **E \_ NOTIMPL**. Solo se llama a **GetSummaryInfo** una vez por cada extensión, no por página, por lo que si la extensión de creación de objetos agrega más de una página, la extensión debe combinar los datos de resumen en una sola cadena.

Cuando el usuario hace clic en el botón **Finalizar** de la página "finalizar", el asistente llama a cada uno de los métodos [**IDsAdminNewObjExt:: WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) de la extensión con el contexto de **\_ \_ \_ preconfirmación DSA NEWOBJ CTX** . Cuando esto ocurre, la extensión debe escribir los datos recopilados en las propiedades adecuadas mediante el método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) o [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) . La interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) se proporciona a la extensión en el método [**IDsAdminNewObjExt:: SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) . La extensión no debe confirmar las propiedades almacenadas en caché mediante una llamada a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo). Cuando se han escrito todas las propiedades, la extensión de creación de objetos principales confirma los cambios mediante una llamada a **IADs:: SetInfo**. Esto se describe con más detalle a continuación.

Si se produce un error, se notificará el error a la extensión y durante la operación que se produjo cuando se llama al método [**IDsAdminNewObjExt:: OnError**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror) .

## <a name="implementing-a-primary-object-creation-wizard"></a>Implementar un asistente para crear un objeto principal

La implementación de un asistente para crear objetos principales es idéntica a la del Asistente para crear objetos secundarios, salvo que un asistente para crear objetos principales debe realizar algunos pasos más.

Antes de descartar la primera página, el Asistente para crear objetos debe crear el objeto de directorio temporal. Para ello, llame al método [**IDsAdminNewObjPrimarySite:: CreateNew**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) . Un puntero a la interfaz [**IDsAdminNewObjPrimarySite**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite) se obtiene llamando a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) con **IID \_ IDsAdminNewObjPrimarySite** en la interfaz [**IDsAdminNewObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj) que se pasa a [**IDsAdminNewObjExt:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize). El método **CreateNew** crea un nuevo objeto temporal y llama a [**IDsAdminNewObjExt:: SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) para cada extensión.

Cuando un asistente para crear objetos contiene más de una página, el sistema implementa una página "finalizar" que muestra un resumen de la información del objeto que se va a guardar. Cuando se hace clic en el botón **Finalizar** de la página "finalizar", el sistema llamará a cada uno de los métodos [**IDsAdminNewObjExt:: WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) de la extensión de creación de objetos y, a continuación, confirmará el objeto temporal en la memoria persistente. Sin embargo, si el Asistente para la creación de objetos solo contiene una página, la página tendrá los botones **Aceptar** y **Cancelar** en lugar de **atrás**, los botones **siguiente** y **Cancelar** se encuentran normalmente en un asistente y no se proporciona ninguna página "finalizar". Por este motivo, un asistente para extensión de creación de objetos de una sola página debe llamar a [**IDsAdminNewObjPrimarySite:: commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) para realizar las operaciones de escritura y guardado. Una extensión de creación de objeto principal de una sola página debe llamar a **commit** en respuesta a la notificación [**\_ WIZFINISH de PSN**](../controls/psn-wizfinish.md) .

Dado que otras extensiones de creación de objetos pueden agregar páginas al asistente, es posible que la extensión de creación de objetos principales no sepa si hay más de una página en el asistente. Esto no es un problema por dos motivos: en primer lugar, si el sistema implementa la página "Finish", la extensión de creación de objeto principal recibirá la notificación [**\_ WIZNEXT de PSN**](../controls/psn-wiznext.md) en lugar de la notificación **\_ WIZNEXT de PSN** . En segundo lugar, la [**confirmación**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) producirá un error inofensivo si el asistente contiene más de una página.

 

 