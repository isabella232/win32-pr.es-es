---
description: El modelo de objetos componentes (COM) es un estándar binario para escribir software de componentes en un entorno informático distribuido.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Copia de seguridad y restauración de la base de datos de registro de clases COM+ en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473406"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a>Copia de seguridad y restauración de la base de datos de registro de clases COM+ en VSS

El modelo de objetos componentes (COM) es un estándar binario para escribir software de componentes en un entorno informático distribuido.

La implementación original de Win32 almacena identificadores de componentes (GUID) y otro estado COM en el Registro en **HKEY \_ CLASSES ROOT \_ \\ CLSID**.

La generación actual del modelo de objetos componentes, COM+, ofrece una base de datos independiente del Registro para almacenar información de registro de componentes: la base de datos de registro de clases COM+.

La base de datos de registro de clases COM+ admite vss writer, que permite a los solicitantes hacer una copia de seguridad de la base de datos de registro mediante los datos almacenados en un volumen de instantáneas.

Para restaurar la base de datos de registro de COM+, un solicitante debe llamar al [método ICOMAdminCatalog::RestoreREGDB.](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb)

Para obtener más información sobre el escritor de base de datos de registro de COM+, vea [In-Box VSS Writers](in-box-vss-writers.md).

 

 
