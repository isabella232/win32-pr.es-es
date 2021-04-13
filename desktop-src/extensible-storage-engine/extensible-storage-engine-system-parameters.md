---
description: 'Más información sobre: parámetros del sistema del motor de almacenamiento extensible'
title: Parámetros del sistema del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544011"
---
# <a name="extensible-storage-engine-system-parameters"></a>Parámetros del sistema del motor de almacenamiento extensible


_**Se aplica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-system-parameters"></a>Parámetros del sistema del motor de almacenamiento extensible

Las constantes siguientes se usan como valores para el parámetro *paramid* de las funciones [JetGetSystemParameter](./jetgetsystemparameter-function.md) y [JetSetSystemParameter](./jetsetsystemparameter-function.md) .

  - [Parámetros de copia de seguridad y restauración](./backup-and-restore-parameters.md)

  - [Parámetros de devolución de llamada](./callback-parameters.md)

  - [Parámetros de base de datos](./database-parameters.md)

  - [Parámetros de caché de base de datos](./database-cache-parameters.md)

  - [Parámetros de control de errores](./error-handling-parameters.md)

  - [Parámetros del registro de eventos](./event-log-parameters.md)

  - [Parámetros de e/s](./i-o-parameters.md)

  - [Parámetros de índice](./index-parameters.md)

  - [Parámetros informativos](./informational-parameters.md)

  - [Metaparámetros](./meta-parameters.md)

  - [Parámetros de recursos](./resource-parameters.md)

  - [Parámetros temporales de base de datos](./temporary-database-parameters.md)

  - [Parámetros de registro de transacciones](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Formato de descripción de parámetros del sistema

Cada parámetro del sistema se describe con el siguiente formato:

JET_paramX

Descripción del parámetro del sistema JET_paramX.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>Valor predeterminado del parámetro.</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>El tipo de datos del parámetro.</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Valores válidos para el parámetro.</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>¿El parámetro es global o por instancia?</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>¿Se puede establecer el parámetro si existe alguna instancia?</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>¿Se puede establecer el parámetro al inicializarse?</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>¿El parámetro afecta a los archivos en el disco?</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>¿Afecta el parámetro a la confiabilidad del motor?</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>¿Afecta el parámetro al rendimiento del motor?</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>¿Afecta el parámetro a los recursos del motor?</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Versiones de Windows que admiten el parámetro.</p></td>
</tr>
</tbody>
</table>
