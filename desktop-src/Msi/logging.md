---
description: Esta directiva de sistema por máquina solo se usa si el registro no se ha habilitado mediante la opción de línea de comandos \# &0034;/L&\# 0034; o msiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registro (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074421"
---
# <a name="logging-windows-installer"></a>Registro (Windows instalador)

Esta directiva de sistema [por](system-policy.md) máquina solo se usa si el registro no se ha habilitado mediante la opción de línea de comandos "/L" o [**msiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga). Si la directiva se establece en este caso, el instalador crea un archivo de registro en %temp% con el nombre aleatorio: MSI \* . REGISTRO. Especifique el modo de registro estableciendo el valor de directiva en una cadena de caracteres. Use los mismos caracteres para especificar la directiva de modo de registro que usa la opción de línea de comandos ["/L".](command-line-options.md) Tenga en cuenta que no puede usar "+" y \* "" para la directiva.

El modo de registro se puede establecer mediante directiva, una opción de línea de comandos o mediante programación. Para obtener más información sobre todos los métodos que están disponibles para establecer el modo de registro, vea [Registro normal](normal-logging.md) en la Windows [registro del](windows-installer-logging.md) instalador.

Puede evitar que la información confidencial, por ejemplo, las contraseñas, se introducen en el archivo de registro y se hacen visibles. Para obtener más información, vea [Impedir que la información confidencial se escriba en el archivo de registro.](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="registry-key"></a>Clave del Registro

Establezca el valor denominado Registro en la siguiente clave del Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ SZ**

 

 



