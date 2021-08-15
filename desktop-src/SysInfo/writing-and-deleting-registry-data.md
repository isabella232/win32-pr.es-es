---
description: Una aplicación puede usar la función RegSetValueEx para asociar un valor y sus datos a una clave. Para obtener una lista de los tipos de valor admitidos por RegSetValueEx, vea Tipos de valor del Registro.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Escritura y eliminación de datos del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd4e80dc3320d1af0931e111c82f473e0edf56ac071443397ffc3da0918f7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883997"
---
# <a name="writing-and-deleting-registry-data"></a>Escritura y eliminación de datos del Registro

Una aplicación puede usar la [**función RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) para asociar un valor y sus datos a una clave. Para obtener una lista de los tipos de valor admitidos por **RegSetValueEx**, vea [Tipos de valor del Registro](registry-value-types.md).

Para eliminar un valor de una clave, una aplicación puede usar la [**función RegDeleteValue.**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) Para eliminar una clave, puede usar la [**función RegDeleteKey.**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) Una clave eliminada no se quita hasta que se haya cerrado el último identificador de ella. Las subclaves y los valores no se pueden crear con una clave eliminada.

No es posible bloquear una clave del Registro durante una operación de escritura para sincronizar el acceso a los datos. Sin embargo, puede controlar el acceso a una clave del Registro mediante atributos de seguridad. Para obtener más información, vea [Derechos de acceso y seguridad de claves del Registro.](registry-key-security-and-access-rights.md)

Se puede realizar más de una operación del Registro dentro de una única transacción. Para asociar una clave del Registro a una transacción, una aplicación puede usar la [**función RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) o [**RegOpenKeyTransacted.**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) Para obtener más información sobre las transacciones, vea [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
