---
description: 'La biblioteca Xenroll.dll contiene los siguientes métodos y propiedades que puede usar para administrar almacenes de certificados. FunctionsDescriptionCAStoreFlagsSpecifies o devuelve marcas que controlan el acceso al almacén de la entidad de certificación (CA). CAStoreNameWStrSpecifies o devuelve el nombre del almacén de CA. CAStoreTypeWStrSpecifies o devuelve el tipo del almacén identificado por la propiedad CAStoreName. MyStoreFlagsSpecifies o devuelve una marca que determina la ruta de acceso del almacén personal. MyStoreNameWStrSpecifies o devuelve el nombre del almacén personal. MyStoreTypeWStrSpecifies o devuelve el tipo del almacén personal. RequestStoreFlagsSpecifies o devuelve una marca que determina la ruta de acceso del almacén de solicitudes. RequestStoreNameWStrSpecifies o devuelve el nombre del almacén de solicitudes. RequestStoreTypeWStrSpecifies o devuelve el tipo del almacén de solicitudes. RootStoreFlagsSpecifies o devuelve una marca que determina la ruta de acceso del almacén raíz. RootStoreNameWStrSpecifies o devuelve el nombre del almacén raíz. RootStoreTypeWStrSpecifies o devuelve el tipo del almacén raíz. SetHStoreCASpecifies identificador del almacén de la entidad de certificación. SetHStoreMySpecifies el identificador del almacén personal. SetHStoreRequestSpecifies identificador del almacén de solicitudes. SetHStoreROOTSpecifies identificador del almacén raíz. '
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: Funciones del almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00ab4b7245f999e1131f41172b3c77af8b9c2aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688055"
---
# <a name="certificate-store-functions"></a>Funciones del almacén de certificados

La biblioteca Xenroll.dll contiene los siguientes métodos y propiedades que puede usar para administrar almacenes de certificados.

| Functions                                                          | Descripción                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | Especifica o devuelve las marcas que controlan el acceso al almacén de la [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA).<br/> |
| [**CAStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | Especifica o devuelve el nombre del almacén de CA.<br/>                                                                                                                                            |
| [**CAStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | Especifica o devuelve el tipo del almacén identificado por la propiedad **CAStoreName** .<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | Especifica o devuelve una marca que determina la ruta de acceso del almacén personal.<br/>                                                                                                               |
| [**MyStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | Especifica o devuelve el nombre del almacén personal.<br/>                                                                                                                                      |
| [**MyStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | Especifica o devuelve el tipo del almacén personal.<br/>                                                                                                                                      |
| [**RequestStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags)       | Especifica o devuelve una marca que determina la ruta de acceso del almacén de solicitudes.<br/>                                                                                                                |
| [**RequestStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr) | Especifica o devuelve el nombre del almacén de solicitudes.<br/>                                                                                                                                       |
| [**RequestStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr) | Especifica o devuelve el tipo del almacén de solicitudes.<br/>                                                                                                                                       |
| [**RootStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags)             | Especifica o devuelve una marca que determina la ruta de acceso del almacén raíz.<br/>                                                                                                                   |
| [**RootStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr)       | Especifica o devuelve el nombre del almacén raíz.<br/>                                                                                                                                          |
| [**RootStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr)       | Especifica o devuelve el tipo del almacén raíz.<br/>                                                                                                                                          |
| [**SetHStoreCA**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca)                   | Especifica el identificador del almacén de CA.<br/>                                                                                                                                                     |
| [**SetHStoreMy**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy)                   | Especifica el identificador del almacén personal.<br/>                                                                                                                                               |
| [**SetHStoreRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest)         | Especifica el identificador del almacén de solicitudes.<br/>                                                                                                                                                |
| [**SetHStoreROOT**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot)               | Especifica el identificador del almacén raíz.<br/>                                                                                                                                                   |



 

CertEnroll.dll no exporta la funcionalidad que le permite especificar o recuperar valores de propiedad del almacén o copiar certificados en almacenes específicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

