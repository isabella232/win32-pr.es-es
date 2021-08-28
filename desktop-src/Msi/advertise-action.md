---
description: La acción ADVERTISE es una acción de nivel superior denominada para instalar o quitar componentes anunciados.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Acción ADVERTISE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd70b36edfb0074911ee3c9487a299f3c0b2eb4bacc59f05241fc6ee22119800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045935"
---
# <a name="advertise-action"></a>Acción ADVERTISE

La acción ADVERTISE es una acción de nivel superior denominada para instalar o quitar componentes anunciados.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

[*La*](a-gly.md) publicidad hace referencia a la capacidad del instalador de proporcionar las interfaces de carga e inicio de una aplicación sin instalar físicamente la aplicación. El instalador no instala los componentes necesarios hasta que un usuario o aplicación activa una interfaz anunciada. Este concepto se denomina [*instalación a petición.*](i-gly.md)

No se llama a la acción ADVERTISE desde la secuencia de la tabla de acciones, el instalador de Windows ejecuta esta acción cuando se llama al ejecutable de línea de comandos Msiexec.exe con el modificador de línea de comandos '/j' o cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) con el *parámetro szCommandLine* establecido en ACTION=ADVERTISE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla AdvtExecuteSequence](advtexecutesequence-table.md)
</dt> </dl>

 

 



