---
description: Una aplicación puede usar la función RegSetValueEx para asociar un valor y sus datos a una clave. Para obtener una lista de los tipos de valor admitidos por RegSetValueEx, vea Tipos de valor del Registro.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Escribir y eliminar datos del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371912"
---
# <a name="writing-and-deleting-registry-data"></a>Escribir y eliminar datos del Registro

Una aplicación puede usar la [**función RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) para asociar un valor y sus datos a una clave. Para obtener una lista de los tipos de valor admitidos **por RegSetValueEx**, vea [Tipos de valor del Registro](registry-value-types.md).

Para eliminar un valor de una clave, una aplicación puede usar la [**función RegDeleteValue.**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) Para eliminar una clave, puede usar la [**función RegDeleteKey.**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) Una clave eliminada no se quita hasta que se ha cerrado el último identificador para ella. Las subclaves y los valores no se pueden crear con una clave eliminada.

No es posible bloquear una clave del Registro durante una operación de escritura para sincronizar el acceso a los datos. Sin embargo, puede controlar el acceso a una clave del Registro mediante atributos de seguridad. Para obtener más información, vea [Derechos de acceso y seguridad de claves del Registro.](registry-key-security-and-access-rights.md)

Se puede realizar más de una operación del Registro dentro de una única transacción. Para asociar una clave del Registro a una transacción, una aplicación puede usar la [**función RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) o [**RegOpenKeyTransacted.**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) Para obtener más información sobre las transacciones, vea [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
