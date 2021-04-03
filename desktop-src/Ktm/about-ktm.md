---
description: El administrador de transacciones de kernel (KTM) es un servicio de administración de transacciones. Hace que las transacciones estén disponibles como objetos de kernel y proporciona servicios de administración de transacciones a los componentes del sistema como NTFS transaccional (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: Acerca de KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083358"
---
# <a name="about-ktm"></a>Acerca de KTM

El administrador de transacciones de kernel (KTM) es un servicio de administración de transacciones. Hace que las transacciones estén disponibles como objetos de kernel y proporciona servicios de administración de transacciones a los componentes del sistema como [NTFS transaccional](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).

En los temas siguientes se describen los usos y las características de KTM:

-   [¿Qué es una transacción?](what-is-a-transaction.md)
-   [Trabajar con transacciones](programming-model.md)
-   [Escribir un Administrador de recursos](writing-a-resource-manager.md)
-   [Interoperabilidad con otras características de Windows](interoperability-with-other-windows-features.md)
-   [Derechos de acceso y seguridad de KTM](ktm-security-and-access-rights.md)

KTM se basa en el [sistema de archivos de registro común](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) para su funcionamiento. CLFS es un sistema de registro que es capaz de habilitar transacciones.

 

 
