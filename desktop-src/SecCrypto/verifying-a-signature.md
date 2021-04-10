---
description: Para comprobar una firma, cree un objeto hash mediante CryptCreateHash. Este objeto hash acumula los datos que se van a comprobar. A continuación, los datos se agregan al objeto hash con la función CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Comprobar una firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155072"
---
# <a name="verifying-a-signature"></a>Comprobar una firma

Para comprobar una firma, cree un [*objeto hash*](../secgloss/h-gly.md) mediante [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Este objeto hash acumula los datos que se van a comprobar. A continuación, los datos se agregan al objeto hash con la función [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

Después de agregar el último bloque de datos al hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) para comprobar la firma. La dirección de los datos de la firma, un identificador para el objeto hash y el identificador de las claves públicas se pasan a **CryptVerifySignature**.

Una vez comprobada la firma (o no haya superado la comprobación), destruya el objeto hash mediante la función [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .

 

 
