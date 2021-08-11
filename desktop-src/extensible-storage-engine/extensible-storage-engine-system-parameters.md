---
description: 'Más información sobre: Parámetros del sistema Storage motor extensible'
title: Parámetros extensibles Storage del sistema del motor de base de datos
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
ms.openlocfilehash: 531e599c66279312f80216f1eb09fc612636821227e76f3572645ab6b4ee5137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256456"
---
# <a name="extensible-storage-engine-system-parameters"></a>Parámetros extensibles Storage del sistema del motor de base de datos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine-system-parameters"></a>Parámetros extensibles Storage del sistema del motor de base de datos

Las siguientes constantes se usan como valores para el parámetro *paramid* de las funciones [JetGetSystemParameter](./jetgetsystemparameter-function.md) y [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

  - [Parámetros de copia de seguridad y restauración](./backup-and-restore-parameters.md)

  - [Parámetros de devolución de llamada](./callback-parameters.md)

  - [Parámetros de base de datos](./database-parameters.md)

  - [Parámetros de caché de base de datos](./database-cache-parameters.md)

  - [Parámetros de control de errores](./error-handling-parameters.md)

  - [Parámetros del registro de eventos](./event-log-parameters.md)

  - [Parámetros de E/S](./i-o-parameters.md)

  - [Parámetros de índice](./index-parameters.md)

  - [Parámetros informativos](./informational-parameters.md)

  - [Meta parámetros](./meta-parameters.md)

  - [Parámetros de recursos](./resource-parameters.md)

  - [Parámetros temporales de base de datos](./temporary-database-parameters.md)

  - [Parámetros de registro de transacciones](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Formato de descripción de parámetros del sistema

Cada parámetro del sistema se describirá con el formato siguiente:

JET_paramX

Descripción del parámetro JET_paramX del sistema.

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
<td><p>Los valores legales del parámetro.</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>¿Es el parámetro Global o por instancia?</p></td>
</tr>
<tr class="odd">
<td><p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p></td>
<td><p>¿Se puede establecer el parámetro si existe alguna instancia?</p></td>
</tr>
<tr class="even">
<td><p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p></td>
<td><p>¿Se puede establecer el parámetro cuando se inicializa?</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>¿El parámetro afecta a los archivos del disco?</p></td>
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
<td><p>Versiones de Windows que admiten el parámetro .</p></td>
</tr>
</tbody>
</table>
