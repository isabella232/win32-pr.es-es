---
description: Kernel Transaction Manager (KTM) es un servicio de administración de transacciones. Hace que las transacciones estén disponibles como objetos de kernel y proporciona servicios de administración de transacciones a componentes del sistema como NTFS transaccional (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: Acerca de KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160048"
---
# <a name="about-ktm"></a>Acerca de KTM

Kernel Transaction Manager (KTM) es un servicio de administración de transacciones. Hace que las transacciones estén disponibles como objetos de kernel y proporciona servicios de administración de transacciones a componentes del sistema como [NTFS transaccional](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).

En los temas siguientes se describen los usos y características de KTM:

-   [¿Qué es una transacción?](what-is-a-transaction.md)
-   [Trabajar con transacciones](programming-model.md)
-   [Escribir un Resource Manager](writing-a-resource-manager.md)
-   [Interoperabilidad con otras Windows características](interoperability-with-other-windows-features.md)
-   [Derechos de seguridad y acceso de KTM](ktm-security-and-access-rights.md)

KTM se basa en el [Sistema de archivos de registro común](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) para su funcionamiento. CLFS es un sistema de registro capaz de habilitar transacciones.

 

 
