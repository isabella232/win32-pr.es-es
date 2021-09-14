---
description: La acción ADVERTISE es una acción de nivel superior denominada para instalar o quitar componentes anunciados.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Acción ADVERTISE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159169"
---
# <a name="advertise-action"></a>Acción ADVERTISE

La acción ADVERTISE es una acción de nivel superior denominada para instalar o quitar componentes anunciados.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

[*La*](a-gly.md) publicidad hace referencia a la capacidad del instalador de proporcionar las interfaces de carga e inicio de una aplicación sin instalar físicamente la aplicación. El instalador no instala los componentes necesarios hasta que un usuario o aplicación activa una interfaz anunciada. Este concepto se denomina [*instalación a petición.*](i-gly.md)

No se llama a la acción ADVERTISE desde la secuencia de la tabla de acciones, el instalador de Windows ejecuta esta acción cuando se llama al archivo ejecutable de la línea de comandos Msiexec.exe con el modificador de línea de comandos "/j" o cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) con el *parámetro szCommandLine* establecido en ACTION=ADVERTISE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla AdvtExecuteSequence](advtexecutesequence-table.md)
</dt> </dl>

 

 



