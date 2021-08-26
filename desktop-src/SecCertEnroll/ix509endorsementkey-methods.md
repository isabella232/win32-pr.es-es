---
description: La interfaz IX509EndorsementKey expone los métodos siguientes.
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: Métodos IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83bc951830f308e2918558794c9790c9f57183ca250e17b7821ba2a152428576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881735"
---
# <a name="ix509endorsementkey-methods"></a>Métodos IX509EndorsementKey

La [**interfaz IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expone los métodos siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                        | Descripción                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Método AddCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | Agregue un certificado de clave de aprobación al proveedor de almacenamiento de claves (KSP) que admita claves de aprobación.<br/>                                                                                                                                                                                     |
| [**Método Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | Cierra la clave de aprobación. Solo puede llamar al [**método Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) una vez [**que**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) se haya llamado correctamente al método Open.<br/>                                                                                              |
| [**Método ExportPublicKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | Exporta la clave pública de aprobación.<br/>                                                                                                                                                                                                                                                      |
| [**Método GetCertificateByIndex**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | Obtiene el certificado de aprobación asociado a la clave de aprobación del proveedor de almacenamiento de claves para el índice especificado.<br/>                                                                                                                                                              |
| [**Método GetCertificateCount**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | Obtiene el recuento de los certificados de aprobación en el proveedor de almacenamiento de claves.<br/>                                                                                                                                                                                                              |
| [**Método Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | Abre la clave de aprobación. La clave de aprobación debe estar abierta para poder recuperar una información de la clave de aprobación, agregar o quitar certificados, o exportar la clave de aprobación.<br/>                                                                                                  |
| [**Método RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | Quita un certificado de aprobación relacionado con la clave de aprobación del proveedor de almacenamiento de claves. Solo puede llamar al [**método RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) una vez [**que**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) se haya llamado correctamente al método Open.<br/> |



 

 

 




