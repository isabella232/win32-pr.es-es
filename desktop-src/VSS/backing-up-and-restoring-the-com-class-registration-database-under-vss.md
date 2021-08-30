---
description: El modelo de objetos componentes (COM) es un estándar binario para escribir software de componentes en un entorno informático distribuido.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Copia de seguridad y restauración de la base de datos de registro de clases COM+ en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b248408d3c1a712fa37c55fd851bc7cc72662ac4da91422e6b1086d4b022107
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124585"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a>Copia de seguridad y restauración de la base de datos de registro de clases COM+ en VSS

El modelo de objetos componentes (COM) es un estándar binario para escribir software de componentes en un entorno informático distribuido.

La implementación original de Win32 almacena identificadores de componentes (GUID) y otro estado COM en el Registro en **HKEY \_ CLASSES ROOT \_ \\ CLSID**.

La generación actual del modelo de objetos componentes, COM+, ofrece una base de datos independiente del Registro para almacenar información de registro de componentes: la base de datos de registro de clases COM+.

La base de datos de registro de clases COM+ admite vss writer, que permite a los solicitantes hacer una copia de seguridad de la base de datos de registro mediante los datos almacenados en un volumen de instantáneas.

Para restaurar la base de datos de registro de COM+, un solicitante debe llamar al [método ICOMAdminCatalog::RestoreREGDB.](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb)

Para obtener más información sobre el escritor de base de datos de registro de COM+, vea [In-Box VSS Writers](in-box-vss-writers.md).

 

 
