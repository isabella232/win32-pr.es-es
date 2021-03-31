---
description: La acción anunciar es una acción de nivel superior llamada para instalar o quitar componentes anunciados.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Acción de anuncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813350"
---
# <a name="advertise-action"></a>Acción de anuncio

La acción anunciar es una acción de nivel superior llamada para instalar o quitar componentes anunciados.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La [*publicidad*](a-gly.md) se refiere a la capacidad del instalador de proporcionar las interfaces de carga e inicio de una aplicación sin necesidad de instalar físicamente la aplicación. El instalador no instala los componentes necesarios hasta que un usuario o una aplicación Active una interfaz anunciada. Este concepto se denomina [*instalación a petición*](i-gly.md).

No se llama a la acción de anuncio desde la secuencia de la tabla de acciones, la Windows Installer ejecuta esta acción cuando se llama al Msiexec.exe ejecutable de línea de comandos con el modificador de línea de comandos '/j ' o cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) con el parámetro *SZCOMMANDLINE* establecido en Action = resume.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla AdvtExecuteSequence](advtexecutesequence-table.md)
</dt> </dl>

 

 



