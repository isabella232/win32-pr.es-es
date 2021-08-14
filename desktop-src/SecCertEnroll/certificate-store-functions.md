---
description: 'La Xenroll.dll de certificados contiene los siguientes métodos y propiedades que puede usar para administrar almacenes de certificados. FunctionsDescriptionCAStoreFlags Especifica o devuelve marcas que controlan el acceso al almacén de la entidad de certificación (CA). CAStoreNameWStrSpecifa o devuelve el nombre del almacén de ca. CAStoreTypeWStrSpecifa o devuelve el tipo del almacén identificado por la propiedad CAStoreName. MyStoreFlags Especifica o devuelve una marca que determina la ruta de acceso del almacén personal. MyStoreNameWStr Especifica o devuelve el nombre del almacén personal. MyStoreTypeWStrSpecifa o devuelve el tipo de almacén personal. RequestStoreFlags Especifica o devuelve una marca que determina la ruta de acceso del almacén de solicitudes. RequestStoreNameWStr Especifica o devuelve el nombre del almacén de solicitudes. RequestStoreTypeWStr Especifica o devuelve el tipo del almacén de solicitudes. RootStoreFlags Especifica o devuelve una marca que determina la ruta de acceso del almacén raíz. RootStoreNameWStrSpecifa o devuelve el nombre del almacén raíz. RootStoreTypeWStrSpecifa o devuelve el tipo del almacén raíz. SetHStoreCA Especifica el identificador del almacén de ca. SetHStoreMySpecifa el identificador del almacén personal. SetHStoreRequest Especifica el identificador del almacén de solicitudes. SetHStoreROOT Especifica el identificador del almacén raíz. '
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: Funciones del almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53a90a6fd2146517d4d70f653da42961274301a3058f8dbad9e72b8b90228bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902179"
---
# <a name="certificate-store-functions"></a>Funciones del almacén de certificados

La Xenroll.dll de certificados contiene los siguientes métodos y propiedades que puede usar para administrar almacenes de certificados.

| Functions                                                          | Descripción                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | Especifica o devuelve marcas que controlan el acceso al almacén [*de la*](/windows/desktop/SecGloss/c-gly) entidad de certificación (CA).<br/> |
| [**CAStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | Especifica o devuelve el nombre del almacén de ca.<br/>                                                                                                                                            |
| [**CAStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | Especifica o devuelve el tipo del almacén identificado por la **propiedad CAStoreName.**<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | Especifica o devuelve una marca que determina la ruta de acceso del almacén personal.<br/>                                                                                                               |
| [**MyStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | Especifica o devuelve el nombre del almacén personal.<br/>                                                                                                                                      |
| [**MyStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | Especifica o devuelve el tipo de almacén personal.<br/>                                                                                                                                      |
| [**RequestStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags)       | Especifica o devuelve una marca que determina la ruta de acceso del almacén de solicitudes.<br/>                                                                                                                |
| [**RequestStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr) | Especifica o devuelve el nombre del almacén de solicitudes.<br/>                                                                                                                                       |
| [**RequestStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr) | Especifica o devuelve el tipo del almacén de solicitudes.<br/>                                                                                                                                       |
| [**RootStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags)             | Especifica o devuelve una marca que determina la ruta de acceso del almacén raíz.<br/>                                                                                                                   |
| [**RootStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr)       | Especifica o devuelve el nombre del almacén raíz.<br/>                                                                                                                                          |
| [**RootStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr)       | Especifica o devuelve el tipo del almacén raíz.<br/>                                                                                                                                          |
| [**SetHStoreCA**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca)                   | Especifica el identificador del almacén de ca.<br/>                                                                                                                                                     |
| [**SetHStoreMy**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy)                   | Especifica el identificador del almacén personal.<br/>                                                                                                                                               |
| [**SetHStoreRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest)         | Especifica el identificador del almacén de solicitudes.<br/>                                                                                                                                                |
| [**SetHStoreROOT**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot)               | Especifica el identificador del almacén raíz.<br/>                                                                                                                                                   |



 

CertEnroll.dll no exporta la funcionalidad que le permite especificar o recuperar valores de propiedad de almacén o copiar certificados en almacenes específicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

