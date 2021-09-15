---
description: Un proveedor de métodos permite el acceso WMI a los métodos de una clase . Por ejemplo, una clase que representa una aplicación puede tener un método que finaliza la aplicación.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Escribir un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569677"
---
# <a name="writing-a-method-provider"></a>Escribir un proveedor de métodos

Un proveedor de métodos permite el acceso WMI a los métodos de una clase . Por ejemplo, una clase que representa una aplicación puede tener un método que finaliza la aplicación.

Cambiar el orden de los parámetros de entrada y salida del método al actualizar un proveedor de métodos existente puede provocar un error en las aplicaciones que llaman al método . El orden de los parámetros de entrada o salida se establece mediante el valor del calificador [**de identificador**](standard-wmi-qualifiers.md) en cada parámetro. El primer parámetro tiene un **valor de identificador** de cero. Agregue nuevos parámetros de entrada al final de los parámetros existentes en lugar de insertarlos en la secuencia ya establecida.

En el procedimiento siguiente se describe cómo implementar un proveedor de métodos.

**Para implementar un proveedor de métodos**

1.  Diseñe y registre el proveedor de clases con WMI.

    Los proveedores de clases se registran con WMI mediante la creación de una [**\_ \_ instancia de Win32Provider**](--win32provider.md) y [**\_ \_ una clase MethodProviderRegistration.**](--methodproviderregistration.md) Para obtener más información, vea [Registrar un proveedor de métodos](registering-a-method-provider.md).

2.  Implemente [**la interfaz IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    > [!Note]  
    > Se recomienda encarecidamente a los proveedores de métodos que usen el modelo multithreading "Both".

     

3.  Implemente [**el método IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para el proveedor.

    La [**interfaz IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) es la interfaz principal de un proveedor de métodos. Para obtener más información, vea [Implementar la interfaz principal para un proveedor de métodos](implementing-the-primary-interface-for-a-method-provider.md).

4.  Agregue cualquier código adicional necesario para el proveedor.

    Al diseñar el proveedor, lo más probable es que deba llamar a interfaces WMI. Para obtener más información, vea [Llamar a un método](calling-a-method.md) y mantener los niveles de seguridad en un [proveedor](impersonating-a-client.md).

    Al recuperar información para un cliente, es posible que tenga que acceder a los niveles de seguridad de ese cliente. Para obtener más información, [vea Suplantación de un cliente.](impersonating-a-client.md)

5.  Reemplace el proveedor preexistnte por el nuevo código.

    No es necesario realizar este paso si no tiene un proveedor preexistnte sobre el que copiar. Para obtener más información, vea [Actualizar un proveedor](updating-a-provider.md).

 

 



