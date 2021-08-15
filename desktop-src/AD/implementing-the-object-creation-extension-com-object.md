---
title: Implementar el objeto COM de la extensión de creación de objetos
description: Una extensión de creación de objetos es un objeto COM implementado como un servidor en proceso. Las extensiones de creación de objetos principales y secundarios deben implementar la interfaz IDsAdminNewObjExt.
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- Implementar la extensión de creación de objetos COM AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c1d7eb9d3e2fe80e721068f39746e08f0ecf5a1db721658c02ec52aca39687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187643"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>Implementar el objeto COM de la extensión de creación de objetos

Una extensión de creación de objetos es un objeto COM implementado como un servidor en proceso. Las extensiones de creación de objetos principales y secundarios deben implementar la [**interfaz IDsAdminNewObjExt.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext)

## <a name="implementing-idsadminnewobjext"></a>Implementación de los IDsAdminNewObjExt

Cuando se crea el asistente para la creación de objetos, inicializa cada extensión de creación de objetos mediante una llamada al método [**IDsAdminNewObjExt::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) de la extensión. El **método Initialize** proporciona a la extensión información sobre el contenedor en el que se crea el objeto, el nombre de clase del nuevo objeto e información sobre el propio asistente. Si se inicia el Asistente para la creación de objetos para crear un nuevo objeto a partir de un objeto existente, el *parámetro pADsCopySource* no será **NULL.** En este caso, la extensión debe intentar obtener tantos datos del objeto que se va a copiar como sea factible.

Una vez inicializada la extensión, se llama al método [**IDsAdminNewObjExt::AddPages.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) La extensión debe agregar la página o páginas al asistente durante este método. Una página del asistente se crea rellenando una [**estructura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) y, a continuación, pasando esta estructura a la [**función CreatePropertySheetPage.**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) A continuación, la página se agrega al asistente mediante una llamada a la función de devolución de llamada que se pasa a **AddPages** en el *parámetro lpfnAddPage.*

Antes de que se muestre la página de extensión, se llama a [**IDsAdminNewObjExt::SetObject.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) Esto proporciona a la extensión un puntero de interfaz [**IAD para**](/windows/desktop/api/iads/nn-iads-iads) el objeto que se va a crear.

Mientras se muestra la página del asistente, la página debe controlar y responder a los mensajes de notificación del asistente necesarios, como [**PSN \_ SETACTIVE**](../controls/psn-setactive.md) y [**PSN \_ WIZNEXT.**](../controls/psn-wiznext.md)

Cuando el usuario complete todas las páginas del asistente, el asistente mostrará una página "Finalizar" que proporciona un resumen de los datos especificados. El asistente obtiene estos datos llamando al método [**IDsAdminNewObjExt::GetSummaryInfo**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) para cada una de las extensiones. El **método GetSummaryInfo** proporciona un **BSTR** que contiene los datos de texto que se muestran en la página "Finalizar". Una extensión de creación de objetos no tiene que proporcionar datos de resumen. En este caso, **GetSummaryInfo debe** devolver **E \_ NOTIMPL**. **GetSummaryInfo** solo se llama una vez por cada extensión, no por página, por lo que si la extensión de creación de objetos agrega más de una página, la extensión debe combinar los datos de resumen en una cadena.

Cuando el usuario  hace clic en el botón Finalizar de la página "Finalizar", el asistente llama a cada uno de los [**métodos IDsAdminNewObjExt::WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) de la extensión con el contexto PRECOMMIT de **DSA \_ NEWOBJ \_ CTX. \_** Cuando esto sucede, la extensión debe escribir los datos recopilados en las propiedades adecuadas mediante el método [**IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) o [**IADs::P utEx.**](/windows/desktop/api/iads/nf-iads-iads-putex) La [**interfaz IADs**](/windows/desktop/api/iads/nn-iads-iads) se proporciona a la extensión en el método [**IDsAdminNewObjExt::SetObject.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) La extensión no debe confirmar las propiedades almacenadas en caché llamando [**a IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo). Cuando se han escrito todas las propiedades, la extensión de creación del objeto principal confirma los cambios mediante una llamada a **IADs::SetInfo**. Esto se describe con más detalle a continuación.

Si se produce un error, se notificará a la extensión el error y durante qué operación se produjo cuando se llama al método [**IDsAdminNewObjExt::OnError.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror)

## <a name="implementing-a-primary-object-creation-wizard"></a>Implementar un Asistente para la creación de objetos primarios

La implementación de un asistente para la creación de objetos principal es idéntica a la de un asistente para la creación de objetos secundarios, salvo que un asistente para la creación de objetos primarios debe realizar algunos pasos más.

Antes de que se descarte la primera página, el Asistente para la creación de objetos debe crear el objeto de directorio temporal. Para ello, llame al [**método IDsAdminNewObjPrimarySite::CreateNew.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) Para obtener un puntero a la interfaz [**IDsAdminNewObjPrimarySite,**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite) se llama a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) con **IID \_ IDsAdminNewObjPrimarySite** en la interfaz [**IDsAdminNewObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj) que se pasa a [**IDsAdminNewObjExt::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize). El **método CreateNew** crea un nuevo objeto temporal y llama a [**IDsAdminNewObjExt::SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) para cada extensión.

Cuando un asistente para la creación de objetos contiene más de una página, el sistema implementa una página "Finalizar" que muestra un resumen de la información del objeto que se va a guardar. Cuando  se hace clic en el botón Finalizar de la página "Finalizar", el sistema llamará a cada uno de los identificadores del método [**IDsAdminNewObjExt::WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) de la extensión de creación de objetos y, a continuación, confirmará el objeto temporal en la memoria persistente. Sin embargo, si el Asistente para la creación  de  objetos solo contiene una  página, la página tendrá los botones Aceptar y Cancelar en lugar de los botones Atrás **,** Siguiente y Cancelar que normalmente se encuentran en un asistente y no se proporciona ninguna página "Finalizar".  Por este problema, un asistente para la extensión de creación de objetos de página única debe llamar a [**IDsAdminNewObjPrimarySite::Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) para realizar las operaciones de escritura y guardado. Una extensión de creación de objetos primarios de página única debe llamar a **Commit** en respuesta a la [**notificación \_ WIZFINISH de PSN.**](../controls/psn-wizfinish.md)

Dado que otras extensiones de creación de objetos pueden agregar páginas al asistente, es posible que la extensión de creación de objetos principal no sepa si hay más de una página en el asistente. Esto no es un problema por dos motivos: en primer lugar, si el sistema implementa la página "Finalizar", la extensión de creación del objeto principal recibirá la notificación [**\_ WIZNEXT**](../controls/psn-wiznext.md) de PSN en lugar de la notificación **\_ WIZNEXT de PSN.** En segundo lugar, [**la**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) confirmación producirá un error inofensivo si el asistente contiene más de una página.

 

 