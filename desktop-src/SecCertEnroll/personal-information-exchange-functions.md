---
description: En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll para administrar mensajes de personal information Exchange (PFX).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funciones de información personal Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171217"
---
# <a name="personal-information-exchange-functions"></a>Funciones de información personal Exchange

En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll para administrar mensajes de personal information Exchange (PFX). En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o indica que no existe ninguna asignación entre las dos bibliotecas.

## <a name="createfilepfxwstr"></a>createFilePFXWStr

La [**función createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) de Xenroll.dll una cadena [](/windows/desktop/SecGloss/p-gly) de certificados y una clave privada en un archivo mediante el formato PFX.

La CertEnroll.dll no implementa directamente la funcionalidad para copiar el mensaje PFX en un archivo. Sin embargo, puede usar el método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) en la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para crear un mensaje PFX codificado y escribir una función personalizada para guardar el mensaje en un archivo.

## <a name="createpfxwstr"></a>createPFXWStr

La [**función createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) de Xenroll.dll una cadena de certificados y una clave privada en una cadena de formato PFX.

Puede usar el [**método CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) en la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para crear un mensaje PFX codificado que contenga la cadena de certificados y la clave. Puede especificar una contraseña, opciones de exportación y tipo de codificación. Para recuperar una cadena equivalente a la devuelta de [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pase la marca XCN CRYPT STRING BINARY en el parámetro Encoding del \_ \_ método \_ [**CreatePFX.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
