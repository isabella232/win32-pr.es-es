---
description: El modelo de objetos componentes (COM) es un estándar binario para escribir software de componentes en un entorno de computación distribuida.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Realizar copias de seguridad y restaurar la base de datos de registro de clases COM+ en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697796"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a>Realizar copias de seguridad y restaurar la base de datos de registro de clases COM+ en VSS

El modelo de objetos componentes (COM) es un estándar binario para escribir software de componentes en un entorno de computación distribuida.

Los identificadores de componente almacenados (GUID) de la implementación de Win32 original y otro estado COM del registro en las **\_ clases HKEY \_ raíz \\ CLSID**.

La generación actual del modelo de objetos componentes, COM+, ofrece una base de datos independiente del registro para almacenar información de registro de componentes: la base de datos de registro de clases COM+.

La base de datos de registro de clase COM+ admite una VSS Writer, que permite a los solicitantes realizar copias de seguridad de la base de datos de registro mediante los datos almacenados en un volumen de copia sombra.

Para restaurar la base de datos de registro de COM+, un solicitante debe llamar al método [ICOMAdminCatalog:: RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .

Para obtener más información acerca del escritor de bases de datos de registro de COM+, consulte [escritores de VSS en la caja](in-box-vss-writers.md).

 

 
