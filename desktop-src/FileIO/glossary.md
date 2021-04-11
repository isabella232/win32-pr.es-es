---
description: Terminología usada para describir NTFS transaccional (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glosario de TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278818"
---
# <a name="txf-glossary"></a>Glosario de TxF

<dl> <dt>

<span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**disponibilidad**
</dt> <dd>

La disponibilidad significa que un administrador de recursos anulará las transacciones aunque esto interrumpa la coherencia para que el sistema pueda continuar realizando el nuevo trabajo. El administrador de recursos predeterminado fuerza la disponibilidad en el volumen del sistema. Por ejemplo, si el registro de transacciones está lleno, no se puede Agregar un nuevo espacio de registro de transacciones y una transacción más antigua que se anularía requiere la entrega de un resultado desde un administrador de recursos superior para que se complete una transacción distribuida, el administrador de recursos no esperará el administrador de transacciones superior y anulará la transacción aunque pueda interrumpir la coherencia.

</dd> <dt>

<span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**réplica**
</dt> <dd>

La coherencia significa que un administrador de recursos producirá un error en las transacciones nuevas si no puede progresar. Por ejemplo, si el registro de transacciones está lleno, no se puede Agregar un nuevo espacio de registro de transacciones y una transacción anterior que se anularía requiere que se entregue un resultado desde un administrador de recursos superior para que se complete una transacción distribuida, el administrador de recursos esperará ese resultado.

</dd> <dt>

<span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversión**
</dt> <dd>

Una miniversión es una versión de un archivo que un escritor de transacciones crea durante una transacción. La miniversión se puede abrir más adelante en la transacción con acceso de solo lectura.

</dd> <dt>

<span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**lector de transacciones**
</dt> <dd>

Un lector de transacciones es un identificador de archivo de transacción abierto con cualquier permiso que forma parte del acceso de lectura genérico, pero no forma parte del acceso de escritura genérico.

</dd> <dt>

<span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**escritor de transacciones**
</dt> <dd>

Un escritor de transacciones es un identificador de archivo de transacciones abierto con cualquier permiso que no forma parte del acceso de lectura genérico, pero que forma parte del acceso de escritura genérico.

</dd> </dl>

 

 



