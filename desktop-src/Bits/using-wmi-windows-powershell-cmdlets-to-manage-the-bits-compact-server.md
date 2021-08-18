---
title: Uso de cmdlets Windows PowerShell WMI para administrar el servidor de BITS Compact
description: Windows PowerShell proporciona un mecanismo sencillo para conectarse a Windows Management Instrumentation (WMI) en un equipo remoto y administrar el servidor compact de Servicio de transferencia inteligente en segundo plano (BITS).
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e82401e80b5e49b7d2b964ec910d15d70aea7ce9c782a0173bef97aa8b3a5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021083"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>Uso de cmdlets Windows PowerShell WMI para administrar el servidor de BITS Compact

Windows PowerShell proporciona un mecanismo sencillo para conectarse a Windows Management Instrumentation (WMI) en un equipo remoto y administrar el servidor compact de Servicio de transferencia inteligente en segundo plano (BITS). BITS Compact Server es un componente de servidor opcional que se debe instalar por separado. Para obtener información sobre cómo instalar Compact Server, consulte la [documentación de BITS Compact Server.](bits-compact-server.md)

1.  Conectar al proveedor de BITS.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    El cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita las credenciales del usuario para conectarse al equipo remoto y asigna las credenciales al objeto $cred usuario.

    Los objetos devueltos por el cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) se asignan a $bcs variable. En el ejemplo anterior, el cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) recupera la clase [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) en el espacio de nombres bits de \\ Microsoft raíz de \\ Server1. Se puede llamar a métodos estáticos expuestos por la clase [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) en $bcs objeto . Para obtener más información sobre la administración remota de BITS, vea [Proveedor de BITS](/previous-versions/windows/desktop/bitsprov/bits-provider) y Clases de proveedor de [BITS]( /previous-versions//dd904507(v=vs.85)).

    > [!Note]  
    > El carácter de acento grave ( \` ) se usa para indicar un salto de línea.

     

2.  Cree un grupo de direcciones URL en el servidor.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    La cadena https://Server1:80/testurlgroup de prefijo de dirección URL "" se asigna a $URLGroup variable. La $URLGroup variable se pasa al [método CreateUrlGroup,](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) que crea el grupo de direcciones URL en Server1.

    Puede especificar un grupo de direcciones URL diferente. El grupo de direcciones URL debe cumplir una cadena de prefijo de dirección URL válida. Para obtener más información sobre los prefijos de dirección URL, [vea UrlPrefix Strings](../http/urlprefix-strings.md).

3.  Hospedar un archivo en el grupo de direcciones URL.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    La instancia bitsCompactServerUrlGroup devuelta por el cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) se asigna a la variable $bcsObj. Se llama al método [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) para el $bcsObj con el sufijo de dirección URL "url.txt", la ruta de acceso de origen "c: temp1.txt" para el archivo y una cadena de descriptor de seguridad vacía como \\ \\ \\ \\ parámetros. El sufijo "url.txt" se agrega al prefijo del grupo de direcciones URL. Los clientes pueden descargar el archivo desde la siguiente dirección: https://Server1:80/testurlgroup/url.txt .

4.  Limpie la dirección URL y el grupo de direcciones URL.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    El **método system.object Delete** elimina el $bcsObj objeto .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[BITS Compact Server](./bits-compact-server.md)
</dt> <dt>

[Proveedor de BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[Clases de proveedor de BITS]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 