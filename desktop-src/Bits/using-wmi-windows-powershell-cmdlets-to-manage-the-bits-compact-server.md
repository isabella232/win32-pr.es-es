---
title: Usar cmdlets de WMI de Windows PowerShell para administrar el servidor de BITS Compact
description: Windows PowerShell proporciona un mecanismo sencillo para conectarse a Instrumental de administración de Windows (WMI) en un equipo remoto y administrar el servidor de Servicio de transferencia inteligente en segundo plano (BITS) Compact.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995424"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>Usar cmdlets de WMI de Windows PowerShell para administrar el servidor de BITS Compact

Windows PowerShell proporciona un mecanismo sencillo para conectarse a Instrumental de administración de Windows (WMI) en un equipo remoto y administrar el servidor de Servicio de transferencia inteligente en segundo plano (BITS) Compact. El servidor BITS Compact es un componente de servidor opcional que se debe instalar por separado. Para obtener información acerca de cómo instalar el servidor compacto, consulte la documentación del [servidor de bits Compact](bits-compact-server.md) .

1.  Conéctese al proveedor BITS.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    El cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita las credenciales del usuario para conectarse al equipo remoto y asigna las credenciales al objeto $cred.

    Los objetos devueltos por el cmdlet [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) se asignan a la variable $BCS. En el ejemplo anterior, el cmdlet [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) recupera la clase [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) en el \\ \\ espacio de nombres de Microsoft bits raíz de server1. Se puede llamar a los métodos estáticos expuestos por la clase [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) en el objeto $BCS. Para obtener más información acerca de la administración remota de BITS, consulte [clases]( /previous-versions//dd904507(v=vs.85))de proveedor bits [y proveedor bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .

    > [!Note]  
    > El carácter de acento grave ( \` ) se usa para indicar un salto de línea.

     

2.  Cree un grupo de direcciones URL en el servidor.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    La https://Server1:80/testurlgroup cadena de prefijo de dirección URL "" se asigna a la variable $URLGroup. La variable $URLGroup se pasa al método [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , que crea el grupo de direcciones URL en server1.

    Puede especificar un grupo de direcciones URL diferente. El grupo de direcciones URL debe ajustarse a una cadena de prefijo de dirección URL válida. Para obtener más información sobre los prefijos de dirección URL, vea [UrlPrefix Strings](../http/urlprefix-strings.md).

3.  Hospede un archivo en el grupo de direcciones URL.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    La instancia de BITSCompactServerUrlGroup devuelta por el cmdlet [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) se asigna a la variable $bcsObj. Se llama al método [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) para el $bcsObj con el sufijo de dirección URL "url.txt", la \\ \\ ruta de acceso de origen "c: Temp \\ \\1.txt" para el archivo y una cadena de descriptor de seguridad vacía como parámetros. El sufijo "url.txt" se agrega al prefijo del grupo de direcciones URL. Los clientes pueden descargar el archivo de la siguiente dirección: https://Server1:80/testurlgroup/url.txt .

4.  Limpie la dirección URL y el grupo de direcciones URL.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    El método **System. Object Delete** elimina el objeto de $bcsObj.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servidor BITS compacto](./bits-compact-server.md)
</dt> <dt>

[Proveedor BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[Clases de proveedor BITS]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 