---
description: Los certificados de cliente y de servidor deben almacenarse en un almacén de certificados al que pueda acceder el proceso de aplicación.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082403"
---
# <a name="certificate-stores"></a>Almacenes de certificados

Los certificados de [*cliente*](/windows/desktop/SecGloss/c-gly) y de [*servidor*](/windows/desktop/SecGloss/s-gly) deben almacenarse en un [*almacén de certificados*](/windows/desktop/SecGloss/c-gly) al que pueda acceder el proceso de aplicación. Normalmente, se trata de la tienda My, también conocida como el almacén personal. Las aplicaciones cliente como Internet Explorer suelen usar el almacén My del usuario actual, mientras que los servidores como Internet Information Services (IIS) usan el almacén del sistema My del equipo local.

El almacén raíz y el almacén de la [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA) se usan cuando Schannel o una aplicación compilan una cadena de certificados que se va a enviar al equipo remoto. Estos almacenes se usan para validar una cadena de certificados recibida. Para obtener más información, vea [realizar la autenticación con Schannel](performing-authentication-using-schannel.md).

 

 
