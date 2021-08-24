---
description: Los certificados de cliente y de servidor deben almacenarse en un almacén de certificados al que pueda acceder el proceso de aplicación.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64451ea7f568bb5e86289d5d9f1587d98b65aa1d53c14a4a251a5e61fe72b21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883495"
---
# <a name="certificate-stores"></a>Almacenes de certificados

Los [*certificados de*](/windows/desktop/SecGloss/c-gly) cliente y de [*servidor*](/windows/desktop/SecGloss/s-gly) deben almacenarse en un almacén de certificados al [*que*](/windows/desktop/SecGloss/c-gly) pueda acceder el proceso de aplicación. Normalmente, se trata de la tienda Mi, también conocida como almacén personal. Las aplicaciones cliente como Internet Explorer suelen usar el almacén Mi del usuario actual, mientras que servidores como Internet Information Services (IIS) usan el sistema Mi almacén del equipo local.

El almacén raíz y [*el almacén de*](/windows/desktop/SecGloss/c-gly) la entidad de certificación (CA) se usan cuando Schannel o una aplicación compilan una cadena de certificados que se va a enviar al equipo remoto. Estos almacenes se usan para validar una cadena de certificados recibida. Para obtener más información, vea [Realizar la autenticación mediante Schannel.](performing-authentication-using-schannel.md)

 

 
