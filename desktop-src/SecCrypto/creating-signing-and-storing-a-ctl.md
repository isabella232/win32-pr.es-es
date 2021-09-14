---
description: Cree una lista de confianza de certificados firmados (CTL) y guárdela en un almacén de certificados.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Crear, firmar y almacenar una CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259511"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Crear, firmar y almacenar una CTL

En los procedimientos siguientes se crea una lista [*de confianza de*](../secgloss/c-gly.md) certificados (CTL) firmada y se guarda en un almacén de [*certificados*](../secgloss/c-gly.md).

**Para crear y firmar una CTL**

1.  Cree una matriz de elementos que se almacenarán en [*la CTL*](../secgloss/c-gly.md). En el caso de los certificados de confianza, deben ser los hash SHA1 o MD5 de los certificados de confianza.
2.  Inicialice una [**estructura CTL \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) que incluya la matriz de elementos que acaba de crear.
3.  Inicialice una [**estructura \_ CMSG SIGNED \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)
4.  Llame [**a CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl). Esta llamada de función devuelve un puntero a una CTL con codificación firmada (en formato PKCS 7) que contiene la lista de elementos creados \# en el paso 1.

**Para agregar una CTL a un almacén de certificados**

1.  Obtiene un puntero a una CTL firmada y codificada.
2.  Abra el almacén de certificados de destino con una llamada a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
3.  Llame [**a CertAddEncodedCTLToStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

 

 
