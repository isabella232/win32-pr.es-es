---
description: La interfaz IX509EndorsementKey expone las siguientes propiedades.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Propiedades IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41d135205680e4c998c1157844cfa66a9ef9bd7ef4df5ff8258a31e562a685e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117776193"
---
# <a name="ix509endorsementkey-properties"></a>Propiedades IX509EndorsementKey

La [**interfaz IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expone las siguientes propiedades.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propiedad Length**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | Longitud de bits de la clave de aprobación. Solo puede acceder a esta propiedad después de llamar [**al**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) método Open.<br/>                                                                                                                                                                                            |
| [**Propiedad Abierta**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Indica si se ha [**llamado**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) correctamente al método Open.<br/>                                                                                                                                                                                                                                            |
| [**ProviderName, propiedad**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | Nombre del proveedor de cifrado. El valor predeterminado es el proveedor de criptografía de plataforma de Microsoft. Debe establecer la propiedad [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) antes de llamar al [**método Open.**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) No puede cambiar la **propiedad ProviderName** después de llamar al **método Open.**<br/> |



 

 

 




