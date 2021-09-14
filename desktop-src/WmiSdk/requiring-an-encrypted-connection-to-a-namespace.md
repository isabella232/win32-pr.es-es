---
description: Puede requerir que los scripts de cliente y las aplicaciones establezcan una conexión cifrada para la autenticación agregando el calificador RequiresEncryption al archivo .mof de Managed Object Format (MOF) que crea el espacio de nombres.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Requerir una conexión cifrada a un espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063923"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a>Requerir una conexión cifrada a un espacio de nombres

Puede requerir que los scripts de cliente y las aplicaciones establezcan una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo .mof de Managed Object Format (MOF) que crea el espacio de nombres.


Una conexión cifrada a un espacio de nombres WMI especifica **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** (o **PktPrivacy** en un script) para la autenticación. El **calificador RequiresEncryption** hace que WMI rechace las solicitudes de datos entrantes a menos que usen explícitamente la autenticación cifrada. Para obtener más información, vea Establecer el nivel de seguridad [de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md) o Establecer la [autenticación mediante C++.](setting-authentication-using-c-.md)

También puede modificar un espacio de nombres existente agregando este atributo y, a continuación, vuelva a compilar el archivo MOF. **RequiresEncryption se** usa en [*MOF con*](gloss-m.md) la [instrucción de preprocesador pragma namespace.](pragma-namespace.md)

El siguiente procedimiento establece el espacio de nombres para requerir una conexión cifrada.

**Para establecer el cifrado necesario**

1.  Cree un archivo Managed Object Format (MOF) o modifique el archivo MOF existente que defina el espacio de nombres.

    En el ejemplo de código siguiente se muestra que el espacio de nombres que se va a modificar es *root \\ MyNamespace* y el archivo se denomina *MyNamespace \_ security.mof*. **RequiresEncryption tiene** un tipo de datos booleano, por lo que debe establecerse en **True** o **False.**

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  Ejecute [**mofcomp.exe**](mofcomp.md) para compilar el archivo MOF.

    **c: \\ mofcomp MyNamespace \_ security.mof**

    En C++, use los [**métodos IMoFCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

WMI rechaza un cliente que usa el nivel de autenticación predeterminado porque DCOM negocia la seguridad con el nivel requerido por el proceso SVCHOST en el que se ejecuta el servicio WMI. Para obtener más información sobre los hosts de servicio, vea [Provider Hosting and Security](provider-hosting-and-security.md). Para obtener más información sobre cómo establecer niveles de autenticación al conectarse a espacios de nombres WMI, vea Establecer el nivel de seguridad de proceso predeterminado mediante [C++](setting-the-default-process-security-level-using-c-.md), Establecer la autenticación mediante [C++](setting-authentication-using-c-.md)o Establecer el nivel de seguridad de proceso predeterminado [mediante VBScript](setting-the-default-process-security-level-using-vbscript.md).

Al devolver datos en una conexión de devolución de llamada asincrónica, WMI devuelve un mensaje de acceso denegado al equipo solicitante. WMI también realiza una entrada de registro en el registro de eventos NT del equipo con el espacio de nombres cifrado que indica que no se puede establecer una conexión segura con el cliente.

A partir Windows Vista, el archivo WbemCore.log ya no existe. Puede comprobar el registro de eventos NT para ver las entradas que indican las solicitudes de datos entrantes rechazadas a los espacios de nombres que requieren cifrado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer descriptores de seguridad namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[Protección de una conexión WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



