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
ms.openlocfilehash: 6d51d8c918b9c6dfc8f4dde652bbabe7fe3c17ae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475571"
---
# <a name="extensible-storage-engine-system-parameters"></a>Parámetros extensibles Storage del sistema del motor de base de datos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine-system-parameters"></a>Parámetros extensibles Storage del sistema del motor de base de datos

Las constantes siguientes se usan como valores para el parámetro *paramid* de las funciones [JetGetSystemParameter](./jetgetsystemparameter-function.md) y [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

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


| | | <p>Valor predeterminado:</p> | <p>Valor predeterminado del parámetro.</p> | | <p>Escriba:</p> | <p>El tipo de datos del parámetro.</p> | | <p>Intervalo válido:</p> | <p>Los valores legales del parámetro.</p> | | <p>Ámbito:</p> | <p>¿Es el parámetro Global o por instancia?</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>¿Se puede establecer el parámetro si existe alguna instancia?</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>¿Se puede establecer el parámetro cuando se inicializa?</p> | | <p>Afecta al diseño físico:</p> | <p>¿Afecta el parámetro a los archivos del disco?</p> | | <p>Afecta a la confiabilidad:</p> | <p>¿Afecta el parámetro a la confiabilidad del motor?</p> | | <p>Afecta al rendimiento:</p> | <p>¿Afecta el parámetro al rendimiento del motor?</p> | | <p>Afecta a los recursos:</p> | <p>¿Afecta el parámetro a los recursos del motor?</p> | | <p>Disponibilidad:</p> | <p>Versiones de Windows admiten el parámetro .</p> | 

