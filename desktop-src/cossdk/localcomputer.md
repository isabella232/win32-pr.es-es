---
description: Contiene un único objeto que corresponde al equipo al que está accediendo al catálogo. Este objeto contiene información de configuración de nivel de equipo.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Colección LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: b832da702942e8f84baee4303b7fa74a7fd74d683d62534cca619e8c7270e88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813469"
---
# <a name="localcomputer-collection"></a>Colección LocalComputer

Contiene un único objeto que corresponde al equipo al que está accediendo al catálogo. Este objeto contiene información de configuración de nivel de equipo. Si llama al método Conectar en un objeto creado a partir de la clase [**COMAdminCatalog,**](comadmincatalog.md) el objeto de la colección **LocalComputer** contiene información sobre el equipo remoto [**al**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) que está accediendo al catálogo.

Esta colección no admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección LocalComputer** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [ApplicationProxyRSN](#applicationproxyrsn)
-   [CISEnabled](#cisenabled)
-   [DCOMEnabled](#dcomenabled)
-   [DefaultAuthenticationLevel](#defaultauthenticationlevel)
-   [DefaultImpersonationLevel](#defaultimpersonationlevel)
-   [DefaultToInternetPorts](#defaulttointernetports)
-   [Descripción](#description)
-   [DSPartitionLookupEnabled](#dspartitionlookupenabled)
-   [InternetPortsListed](#internetportslisted)
-   [IsRouter](#isrouter)
-   [LoadBalancingCLSID](#loadbalancingclsid)
-   [LocalPartitionLookupEnabled](#localpartitionlookupenabled)
-   [Nombre](#name)
-   [OperatingSystem](#operatingsystem)
-   [PartitionsEnabled](#partitionsenabled)
-   [Puertos](#defaulttointernetports)
-   [ResourcePoolingEnabled](#resourcepoolingenabled)
-   [RPCProxyEnabled](#rpcproxyenabled)
-   [SecureReferencesEnabled](#securereferencesenabled)
-   [SecurityTrackingEnabled](#securitytrackingenabled)
-   [SRPActivateAsActivatorChecks](#srpactivateasactivatorchecks)
-   [SRPRunningObjectChecks](#srprunningobjectchecks)
-   [TransactionTimeout](#transactiontimeout)

### <a name="applicationproxyrsn"></a>ApplicationProxyRSN



| Entrada | Value |
|----------------|------------------------------------------------------------|
| Descripción    | Nombre de servidor remoto que usan los servidores proxy de aplicación de forma predeterminada. |
| Access         | ReadWrite                                                  |
| Tipo           | String                                                     |
| Predeterminado        | ""                                                         |
| Sistema mínimo | Windows 2000                                               |



 

### <a name="cisenabled"></a>CISEnabled



| Entrada | Value |
|----------------|-----------------------------------------------------|
| Descripción    | Indica si los servicios COM de Internet están habilitados. |
| Access         | ReadWrite                                           |
| Tipo           | Bool                                                |
| Valor predeterminado        | False                                               |
| Sistema mínimo | Windows 2000                                        |



 

### <a name="dcomenabled"></a>DCOMEnabled



| Entrada | Value |
|----------------|---------------------------------------------|
| Descripción    | Establezca en True para habilitar DCOM en el equipo. |
| Access         | ReadWrite                                   |
| Tipo           | Bool                                        |
| Valor predeterminado        | Verdadero                                        |
| Sistema mínimo | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nivel de autenticación usado por las aplicaciones que tienen autenticación establecida en Predeterminado. Los valores corresponden a la configuración de autenticación de llamada a procedimiento remoto (RPC).                                                                                         |
| Access         | ReadWrite                                                                                                                                                                                                                                                |
| Tipo           | Valores largos posibles:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6) |
| Valor predeterminado        | COMAdminAuthenticationConnect (2)                                                                                                                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> COMAdminAuthenticationDefault se asigna a COMAdminAuthenticationConnect cuando COM llama [**a CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Se recomienda usar las constantes de la enumeración y no los valores numéricos.

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nivel de suplantación que se permite si no se establece uno.                                                                                                               |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4) |
| Valor predeterminado        | COMAdminImpersonationIdentify (2)                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> Se recomienda usar las constantes de la enumeración y no los valores numéricos.

 

### <a name="defaulttointernetports"></a>DefaultToInternetPorts



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------|
| Descripción    | Determina si el tipo predeterminado de puerto proporcionado debe ser Internet (True) o intranet (False). |
| Access         | ReadWrite                                                                                           |
| Tipo           | Bool                                                                                                |
| Valor predeterminado        | False                                                                                               |
| Sistema mínimo | Windows 2000                                                                                        |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|--------------------------------|
| Descripción    | Descripción del equipo. |
| Access         | ReadWrite                      |
| Tipo           | String                         |
| Predeterminado        | ""                             |
| Sistema mínimo | Windows 2000                   |



 

### <a name="dspartitionlookupenabled"></a>DSPartitionLookupEnabled



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------|
| Descripción    | Indica si el usuario de las asignaciones de particiones está registrado en el almacén de dominios. |
| Access         | ReadWrite                                                                              |
| Tipo           | Bool                                                                                   |
| Valor predeterminado        | Verdadero                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>InternetPortsListed



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si los puertos enumerados en la propiedad Ports se usarán para Internet (True) o para intranet (False). |
| Access         | ReadWrite                                                                                                             |
| Tipo           | Bool                                                                                                                  |
| Valor predeterminado        | False                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>IsRouter



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establezca en True si el equipo es un enrutador para el servicio de equilibrio de carga de componentes (CLB). Esta propiedad solo se puede establecer en True si el servicio de equilibrio de carga de componentes está instalado actualmente en el equipo; de lo contrario, se producen errores con COMADMIN \_ E REQUIERE UNA PLATAFORMA \_ \_ \_ DIFERENTE. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                        |



 

Si esta propiedad se establece en True, el servidor CLB se configura y se inicia en el inicio. El servidor se agrega a la colección ApplicationCluster si aún no está presente.

### <a name="loadbalancingclsid"></a>LoadBalancingCLSID



| Entrada | Value |
|----------------|-------------------------------------|
| Descripción    | CLSID del objeto que se debe equilibrar. |
| Access         | ReadWrite                           |
| Tipo           | String                              |
| Predeterminado        | NULL                                |
| Sistema mínimo | Windows XP                          |



 

### <a name="localpartitionlookupenabled"></a>LocalPartitionLookupEnabled



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------|
| Descripción    | Indica si el usuario de las asignaciones de particiones se registra en el almacén local. |
| Access         | ReadWrite                                                                             |
| Tipo           | Bool                                                                                  |
| Valor predeterminado        | Verdadero                                                                                  |
| Sistema mínimo | Windows Server 2003                                                                   |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del equipo. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                                                 |
| Predeterminado        | "Mi PC"                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Sistema operativo instalado en el equipo local.                                                                                                                                                                                                                                                                                                                                                                                                |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Valores largos posibles:COMAdminOSNotInitialized (0)COMAdminOSWindows3 \_ 1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknow (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16) |
| Valor predeterminado        | COMAdminOSNotInitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>PartitionsEnabled



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si se pueden usar particiones COM+ en el equipo local. Si esta propiedad es False, cualquier intento de usar particiones COM+ produce un error. |
| Access         | ReadWrite                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                    |
| Valor predeterminado        | False                                                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>Puertos



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena que describe los puertos que son para uso de Internet o intranet, en función de la propiedad InternetPortsListed; por ejemplo, "500-599: 600-800". |
| Access         | ReadWrite                                                                                                                                               |
| Tipo           | String                                                                                                                                                  |
| Predeterminado        | ""                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a>ResourcePoolingEnabled



| Entrada | Value |
|----------------|-------------------------------------|
| Descripción    | Habilita el uso de dispensadores de recursos. |
| Access         | ReadWrite                           |
| Tipo           | Bool                                |
| Valor predeterminado        | Verdadero                                |
| Sistema mínimo | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>RPCProxyEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Controla si el proxy DE RPC IIS está habilitado. El proxy DE RPC IIS se usa junto con IIS para reenviar llamadas al mecanismo RPC desde IIS y es una de las partes principales de los servicios de Internet COM, que se habilita estableciendo CISEnabled en True. Para obtener más información sobre RPCProxyEnabled, vea [Http RPC Security](/windows/desktop/Rpc/rpc-over-http-security). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>SecureReferencesEnabled



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Aplica en equipos DCOM que se protegen las llamadas entre procesos a los métodos [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**IUnknown::Release.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) |
| Access         | ReadWrite                                                                                                                                                                 |
| Tipo           | Bool                                                                                                                                                                      |
| Valor predeterminado        | False                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>SecurityTrackingEnabled



| Entrada | Value |
|----------------|---------------------------------------------------------|
| Descripción    | Se establece en True si el seguimiento de seguridad está habilitado en objetos . |
| Access         | ReadWrite                                               |
| Tipo           | Bool                                                    |
| Valor predeterminado        | Verdadero                                                    |
| Sistema mínimo | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina cómo la directiva de restricción de software (SRP) controla las conexiones de activación como activador. Si se establece en True, el nivel de confianza de SRP configurado para el objeto de servidor se compara con el nivel de confianza de SRP del objeto de cliente y el nivel de confianza más alto (más estricto) se usa para ejecutar el objeto de servidor. Si se establece en False, el objeto de servidor se ejecuta con el nivel de confianza SRP del objeto de cliente, independientemente del nivel de confianza de SRP con el que esté configurado el servidor. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Valor predeterminado        | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina cómo la directiva de restricción de software (SRP) controla las conexiones intentadas a los procesos existentes. Si se establece en False, los intentos de conectarse a objetos en ejecución no se comprueban para los niveles de confianza SRP adecuados. Si se establece en True, el objeto en ejecución debe tener un nivel de confianza SRP igual o superior (más estricto) que el objeto de cliente. Por ejemplo, un objeto de cliente con un nivel de confianza SRP sin restricciones no se puede conectar a un objeto en ejecución con un nivel de confianza de SRP no permitido. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Valor predeterminado        | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Debe establecerse en un valor suficiente en segundos si está realizando numerosas operaciones dentro de una transacción. El período de tiempo de espera predeterminado es de 60 segundos y el período de tiempo de espera máximo es de 3600 segundos (1 hora). Si se establece esta propiedad en 0, se deshabilitan los tiempos de espera de las transacciones. Esta propiedad se puede invalidar mediante componentes individuales mediante la propiedad ComponentTransactionTimeout de la [**colección Components.**](components.md) |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Tipo           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Valor predeterminado        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>Ejemplo

En el siguiente ejemplo Visual Basic microsoft muestra cómo conectarse a un equipo remoto y obtener su propiedad SecurityTrackingEnabled mediante la colección **LocalComputer** del equipo remoto. Para usar este ejemplo, agregue la biblioteca de tipos de administrador de COM+ como referencia al Visual Basic proyecto.


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



Para usar la función , proporcione un valor de cadena para el nombre del equipo remoto. En el Visual Basic código siguiente se muestra cómo conectarse al equipo denominado "RemoteComputerName".


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
