---
description: El proveedor base crea claves simétricas de 40 bits creadas con once bytes de sal de valor cero, once bytes de sal distinto de cero si se especifica CRYPT CREATE SALT o ningún valor \_ \_ sal.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Funcionalidad de valor salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f911815152861921f1ffe12090c88ad4795ba042346aee875138acf591d14671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900375"
---
# <a name="salt-value-functionality"></a>Funcionalidad de valor salt

El proveedor base crea claves [](../secgloss/s-gly.md) simétricas de 40 bits creadas con once bytes de sal de valor [*cero,*](../secgloss/s-gly.md)once bytes de sal distinto de cero si se especifica CRYPT CREATE SALT o ningún valor \_ \_ sal. Sin embargo, una clave simétrica de 40 bits con sal de valor cero no es equivalente a una clave simétrica de 40 bits sin sal. Para la interoperabilidad, las claves deben crearse sin sal. Este problema se debe a una condición predeterminada que solo se produce con claves de exactamente 40 bits. Todas las [*demás longitudes de clave*](../secgloss/k-gly.md) no tienen sal asignada de forma predeterminada.

Tanto los proveedores base como el proveedor extendido pueden usar la marca CRYPT NO SALT para especificar que no se asigne ningún valor salt para una clave simétrica \_ \_ de 40 bits. Las funciones que aceptan esta marca son [**CryptGenKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)y [**CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) De forma predeterminada, estas funciones proporcionan compatibilidad con versiones anteriores para el caso de clave simétrica de 40 bits al continuar con el uso de la sal de valor cero de once bytes.

 

 
