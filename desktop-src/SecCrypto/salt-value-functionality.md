---
description: El proveedor base crea claves simétricas de 40 bits creadas con once bytes de sal de valor cero, once bytes de un valor Salt distinto de cero si \_ \_ se especifica CRYPT Create Salt, o ningún valor Salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Funcionalidad de valores Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360468"
---
# <a name="salt-value-functionality"></a>Funcionalidad de valores Salt

El proveedor base crea [*claves simétricas*](../secgloss/s-gly.md) de 40 bits creadas con once bytes de [*sal*](../secgloss/s-gly.md)de valor cero, once bytes de un valor Salt distinto de cero si \_ \_ se especifica CRYPT Create Salt, o ningún valor Salt. Sin embargo, una clave simétrica de 40 bits con sal de valor cero no es equivalente a una clave simétrica de 40 bits sin sal. Para la interoperabilidad, las claves se deben crear sin sal. Este problema es el resultado de una condición predeterminada que solo se produce con claves de exactamente 40 bits. El resto de las [*longitudes de clave*](../secgloss/k-gly.md) no tienen un valor Salt asignado de forma predeterminada.

Tanto los proveedores de base como el proveedor extendido pueden utilizar la \_ marca CRYPT not \_ sal para especificar que no se asigna ningún valor Salt para una clave simétrica de 40 bits. Las funciones que aceptan esta marca son [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)y [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). De forma predeterminada, estas funciones proporcionan compatibilidad con versiones anteriores para el caso de clave simétrica de 40 bits; para ello, se sigue usando el valor de sal de valor cero de once bytes.

 

 
