---
description: La herramienta SetReg establece el valor de las claves del Registro que controlan el comportamiento del proceso de comprobación del certificado Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Uso de SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127477656"
---
# <a name="using-setreg"></a>Uso de SetReg

La herramienta SetReg establece el valor de las claves del Registro que controlan el comportamiento del proceso de comprobación del certificado Authenticode. Estas claves, denominadas claves de estado de publicación de software, controlan si confiar en una raíz de prueba, permiten la aprobación sin conexión de certificados, prueban las fechas de expiración del certificado y realizan comprobaciones de revocación.

El siguiente comando enumera la sintaxis y las opciones para usar SetReg.

**setreg -?**

El siguiente comando hace que una raíz de prueba sea de confianza. De forma predeterminada, una raíz de prueba no es de confianza. Una vez realizados los cambios en los valores de clave, se muestra una lista del valor actual de todos los valores de clave. Si se **usa la opción -q,** no se muestran los valores de clave.

**setreg 1 TRUE**

El siguiente comando hace que una raíz de prueba no sea de confianza y hace que todas las comprobaciones comprueben la revocación. Se **usa la opción -q** para que no se muestre la lista de valores de clave.

**setreg -q 1 FALSE 3 TRUE**

> [!Note]  
> Los comandos, las opciones y los argumentos no distinguen mayúsculas de minúsculas.

 

 

 



