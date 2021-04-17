---
description: Puede requerir que los scripts y las aplicaciones de cliente establezcan una conexión cifrada para la autenticación agregando el calificador RequiresEncryption al archivo Managed Object Format (MOF). mof que crea el espacio de nombres.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Requerir una conexión cifrada a un espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697732"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a>Requerir una conexión cifrada a un espacio de nombres

Puede requerir que los scripts y las aplicaciones de cliente establezcan una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo Managed Object Format (MOF). mof que crea el espacio de nombres.


Una conexión cifrada a un espacio de nombres WMI especifica la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** (o **PktPrivacy** en un script) para la autenticación. El calificador **RequiresEncryption** hace que WMI rechace las solicitudes de datos entrantes a menos que utilicen explícitamente la autenticación cifrada. Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md) o [establecer la autenticación con C++](setting-authentication-using-c-.md).

También puede modificar un espacio de nombres existente agregando este atributo y, a continuación, compilar de nuevo el archivo MOF. **RequiresEncryption** se utiliza en [*MOF*](gloss-m.md) con la instrucción de preprocesador de [espacio de nombres pragma](pragma-namespace.md) .

En el procedimiento siguiente se establece el espacio de nombres para requerir una conexión cifrada.

**Para establecer el cifrado necesario**

1.  Cree un archivo Managed Object Format (MOF) o modifique el archivo MOF existente que define el espacio de nombres.

    En el ejemplo de código siguiente se muestra que el espacio de nombres que se va a modificar es la *raíz \\ myNameSpace* y el archivo se denomina *myNameSpace \_ Security. mof*. **RequiresEncryption** tiene un tipo de valor Boolean, por lo que debe establecerse en **true** o **false**.

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  Ejecute [**mofcomp.exe**](mofcomp.md) para compilar el archivo MOF.

    **c: \\ MOFCOMP myNameSpace \_ Security. mof**

    En C++, utilice los métodos [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

WMI rechaza un cliente que utiliza el nivel de autenticación predeterminado, ya que DCOM negocia la seguridad al nivel requerido por el proceso SVCHOST en el que se ejecuta el servicio WMI. Para obtener más información sobre los hosts de servicio, consulte [hospedaje y seguridad de proveedores](provider-hosting-and-security.md). Para obtener más información acerca de cómo establecer los niveles de autenticación al conectarse a los espacios de nombres de WMI, vea [establecer el nivel de seguridad de proceso predeterminado con c++](setting-the-default-process-security-level-using-c-.md), [establecer la autenticación con c++](setting-authentication-using-c-.md)o [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

Cuando se devuelven datos en una conexión de devolución de llamada asincrónica, WMI devuelve un mensaje de acceso denegado al equipo que lo solicita. WMI también crea una entrada de registro en el registro de eventos de NT del equipo con el espacio de nombres cifrado que indica que no se puede establecer una conexión segura con el cliente.

A partir de Windows Vista, el archivo WbemCore. log ya no existe. Puede buscar entradas en el registro de eventos de NT que indican las solicitudes de datos de entrada rechazadas a los espacios de nombres que requieren cifrado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[Protección de una conexión WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



