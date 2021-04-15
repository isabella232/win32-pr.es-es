---
description: La interfaz IX509EndorsementKey expone las siguientes propiedades.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Propiedades de IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648486"
---
# <a name="ix509endorsementkey-properties"></a>Propiedades de IX509EndorsementKey

La interfaz [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expone las siguientes propiedades.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propiedad Length**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | Longitud de bit de la clave de aprobación. Solo se puede tener acceso a esta propiedad después de llamar al método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/>                                                                                                                                                                                            |
| [**Propiedad opened**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Indica si se ha llamado correctamente al método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/>                                                                                                                                                                                                                                            |
| [**ProviderName (propiedad)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | Nombre del proveedor de cifrado. El valor predeterminado es el proveedor de criptografía de la plataforma de Microsoft. Debe establecer la propiedad [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) antes de llamar al método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) . No se puede cambiar la propiedad **providerName** después de haber llamado al método **Open** .<br/> |



 

 

 




