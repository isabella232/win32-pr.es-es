---
description: En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll para administrar los mensajes de intercambio de información personal (PFX).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funciones de intercambio de información personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688044"
---
# <a name="personal-information-exchange-functions"></a>Funciones de intercambio de información personal

En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll para administrar los mensajes de intercambio de información personal (PFX). En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o se indica que no existe ninguna asignación entre las dos bibliotecas.

## <a name="createfilepfxwstr"></a>createFilePFXWStr

La función [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) de Xenroll.dll guarda una cadena de certificados y una [*clave privada*](/windows/desktop/SecGloss/p-gly) en un archivo con el formato PFX.

La biblioteca CertEnroll.dll no implementa directamente la funcionalidad para copiar el mensaje PFX en un archivo. Sin embargo, puede usar el método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) en la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para crear un mensaje pfx codificado y escribir una función personalizada para guardar el mensaje en un archivo.

## <a name="createpfxwstr"></a>createPFXWStr

La función [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) de Xenroll.dll guarda una cadena de certificados y una clave privada en una cadena de formato PFX.

Puede usar el método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) en la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para crear un mensaje pfx codificado que contenga la cadena de certificados y la clave. Puede especificar una contraseña, opciones de exportación y tipo de codificación. Para recuperar una cadena que es equivalente a la devuelta por [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pase la \_ marca binaria de cadena de cifrado XCN \_ \_ en el parámetro *Encoding* del método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
