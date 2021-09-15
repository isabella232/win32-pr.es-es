---
description: Cuando un documento o texto necesita tener privacidad protegida por un solo usuario o cuando el documento se va a compartir entre un pequeño grupo de personas que tienen acceso a la misma contraseña secreta, se puede realizar un cifrado o descifrado sencillos.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Cifrar y descifrar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476424"
---
# <a name="encrypting-and-decrypting-data"></a>Cifrar y descifrar datos

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Cuando un documento o texto necesita tener privacidad protegida por un solo usuario o cuando el documento se va a compartir entre un pequeño grupo de personas que tienen acceso a la misma contraseña secreta, se puede realizar un cifrado o descifrado sencillos. CAPICOM no admite el tipo de contenido PkCS 7 EncryptedData, pero usa una estructura ASN no estándar \# para EncryptedData. Por lo tanto, solo CAPICOM puede descifrar un objeto CAPICOM EncryptedData.

En las secciones siguientes se muestran ejemplos de tareas de cifrado y descifrado:

-   [Cifrado de un mensaje en CAPICOM](encrypting-a-message-in-capicom.md)
-   [Descifrar un mensaje en CAPICOM](decrypting-a-message-in-capicom.md)

 

 



