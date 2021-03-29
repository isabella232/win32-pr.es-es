---
description: Una aplicación puede utilizar la función RegSetValueEx para asociar un valor y sus datos con una clave. Para obtener una lista de los tipos de valor admitidos por RegSetValueEx, vea Registry Value Types.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Escribir y eliminar datos del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360605"
---
# <a name="writing-and-deleting-registry-data"></a>Escribir y eliminar datos del registro

Una aplicación puede utilizar la función [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) para asociar un valor y sus datos con una clave. Para obtener una lista de los tipos de valor admitidos por **RegSetValueEx**, vea [Registry Value Types](registry-value-types.md).

Para eliminar un valor de una clave, una aplicación puede usar la función [**error en regdeletevalue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) . Para eliminar una clave, puede usar la función [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) . Una clave eliminada no se quita hasta que se cierra el último identificador de la misma. No se pueden crear subclaves y valores bajo una clave eliminada.

No es posible bloquear una clave del registro durante una operación de escritura para sincronizar el acceso a los datos. Sin embargo, puede controlar el acceso a una clave del registro mediante atributos de seguridad. Para obtener más información, consulte [seguridad y derechos de acceso de la clave del registro](registry-key-security-and-access-rights.md).

Se puede realizar más de una operación del registro dentro de una única transacción. Para asociar una clave del registro a una transacción, una aplicación puede usar la función [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) o [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) . Para obtener más información acerca de las transacciones, consulte [Administrador de transacciones de kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
