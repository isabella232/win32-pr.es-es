---
description: Un proveedor de métodos permite el acceso de WMI a los métodos de una clase. Por ejemplo, una clase que representa una aplicación puede tener un método que finaliza la aplicación.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Escribir un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715816"
---
# <a name="writing-a-method-provider"></a>Escribir un proveedor de métodos

Un proveedor de métodos permite el acceso de WMI a los métodos de una clase. Por ejemplo, una clase que representa una aplicación puede tener un método que finaliza la aplicación.

Si se cambia el orden de los parámetros de entrada y salida del método al actualizar un proveedor de métodos existente, puede producirse un error en las aplicaciones que llaman al método. El orden de los parámetros de entrada o salida lo establece el valor del calificador de [**ID**](standard-wmi-qualifiers.md) . en cada parámetro. El primer parámetro tiene un valor de **identificador** de cero. Agregue nuevos parámetros de entrada al final de los parámetros existentes en lugar de insertarlos en la secuencia ya establecida.

En el procedimiento siguiente se describe cómo implementar un proveedor de métodos.

**Para implementar un proveedor de métodos**

1.  Diseñe y registre el proveedor de clases con WMI.

    Los proveedores de clases se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) . Para obtener más información, vea [registrar un proveedor de métodos](registering-a-method-provider.md).

2.  Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    > [!Note]  
    > Se recomienda encarecidamente a los proveedores de métodos que utilicen el modelo de multithreading "both".

     

3.  Implemente el método [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para el proveedor.

    La interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) es la interfaz principal para un proveedor de métodos. Para obtener más información, vea [implementar la interfaz principal para un proveedor de métodos](implementing-the-primary-interface-for-a-method-provider.md).

4.  Agregue el código adicional necesario para el proveedor.

    Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI. Para obtener más información, consulte [llamar a un método](calling-a-method.md) y [mantener los niveles de seguridad en un proveedor](impersonating-a-client.md).

    Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente. Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).

5.  Reemplace el proveedor preexistente con el código nuevo.

    No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia. Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).

 

 



