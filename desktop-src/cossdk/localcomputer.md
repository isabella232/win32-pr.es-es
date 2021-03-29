---
description: Contiene un solo objeto que corresponde al equipo cuyo catálogo está accediendo. Este objeto contiene información de configuración de nivel de equipo.
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
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807898"
---
# <a name="localcomputer-collection"></a>Colección LocalComputer

Contiene un solo objeto que corresponde al equipo cuyo catálogo está accediendo. Este objeto contiene información de configuración de nivel de equipo. Si llama al método [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) en un objeto creado a partir de la clase [**COMAdminCatalog**](comadmincatalog.md) , el objeto de la colección **LocalComputer** contiene información sobre el equipo remoto cuyo catálogo está accediendo.

Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **LocalComputer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

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
-   [Identifica](#operatingsystem)
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
| Descripción    | Nombre del servidor remoto que usan los proxies de aplicación de forma predeterminada. |
| Access         | ReadWrite                                                  |
| Tipo           | String                                                     |
| Predeterminado        | ""                                                         |
| Sistema mínimo | Windows 2000                                               |



 

### <a name="cisenabled"></a>CISEnabled



| Entrada | Value |
|----------------|-----------------------------------------------------|
| Descripción    | Indica si los servicios de Internet de COM están habilitados. |
| Access         | ReadWrite                                           |
| Tipo           | Bool                                                |
| Valor predeterminado        | False                                               |
| Sistema mínimo | Windows 2000                                        |



 

### <a name="dcomenabled"></a>DCOMEnabled



| Entrada | Value |
|----------------|---------------------------------------------|
| Descripción    | Establézcalo en true para habilitar DCOM en el equipo. |
| Access         | ReadWrite                                   |
| Tipo           | Bool                                        |
| Valor predeterminado        | True                                        |
| Sistema mínimo | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nivel de autenticación que usan las aplicaciones que tienen autenticación establecida en el valor predeterminado. Los valores corresponden a la configuración de autenticación de llamada a procedimiento remoto (RPC).                                                                                         |
| Access         | ReadWrite                                                                                                                                                                                                                                                |
| Tipo           | Valores posibles largos: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6) |
| Valor predeterminado        | COMAdminAuthenticationConnect (2)                                                                                                                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> COMAdminAuthenticationDefault se asigna a COMAdminAuthenticationConnect cuando COM llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Se recomienda usar las constantes en la enumeración y no los valores numéricos.

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nivel de suplantación para permitir si no se establece uno.                                                                                                               |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Valores posibles largos: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4) |
| Valor predeterminado        | COMAdminImpersonationIdentify (2)                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> Se recomienda usar las constantes de la enumeración, y no los valores numéricos.

 

### <a name="defaulttointernetports"></a>DefaultToInternetPorts



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------|
| Descripción    | Determina si el tipo predeterminado de Puerto proporcionado debe ser Internet (true) o intranet (false). |
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
| Descripción    | Indica si el usuario de las asignaciones de particiones está protegido en el almacén de dominio. |
| Access         | ReadWrite                                                                              |
| Tipo           | Bool                                                                                   |
| Valor predeterminado        | True                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>InternetPortsListed



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si los puertos enumerados en la propiedad Ports se van a usar para Internet (true) o para intranet (false). |
| Access         | ReadWrite                                                                                                             |
| Tipo           | Bool                                                                                                                  |
| Valor predeterminado        | False                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>IsRouter



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establézcalo en true si el equipo es un enrutador para el servicio de equilibrio de carga de componentes (CLB). Esta propiedad solo se puede establecer en true si el servicio de equilibrio de carga de componentes está instalado actualmente en el equipo; de lo contrario, los errores con COMAdmin \_ E \_ requieren una \_ \_ plataforma diferente. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                        |



 

Si esta propiedad se establece en true, el servidor CLB se configura y se inicia en el inicio. El servidor se agrega a la colección ApplicationCluster si aún no está presente.

### <a name="loadbalancingclsid"></a>LoadBalancingCLSID



| Entrada | Value |
|----------------|-------------------------------------|
| Descripción    | CLSID del objeto que se va a equilibrar. |
| Access         | ReadWrite                           |
| Tipo           | String                              |
| Predeterminado        | NULL                                |
| Sistema mínimo | Windows XP                          |



 

### <a name="localpartitionlookupenabled"></a>LocalPartitionLookupEnabled



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------|
| Descripción    | Indica si el usuario de las asignaciones de particiones está protegido en el almacén local. |
| Access         | ReadWrite                                                                             |
| Tipo           | Bool                                                                                  |
| Valor predeterminado        | True                                                                                  |
| Sistema mínimo | Windows Server 2003                                                                   |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del equipo. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                                                 |
| Predeterminado        | "Mi PC"                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El sistema operativo instalado en el equipo local.                                                                                                                                                                                                                                                                                                                                                                                                |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Valores posibles largos: COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16) |
| Valor predeterminado        | COMAdminOSNotInitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>PartitionsEnabled



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si se pueden usar particiones COM+ en el equipo local. Si esta propiedad es false, cualquier intento de usar particiones COM+ produce un error. |
| Access         | ReadWrite                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                    |
| Valor predeterminado        | False                                                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>Puertos



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena que describe los puertos que son para el uso de Internet o de la intranet, dependiendo de la propiedad InternetPortsListed. por ejemplo, "500-599:600-800". |
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
| Valor predeterminado        | True                                |
| Sistema mínimo | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>RPCProxyEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Controla si el proxy IIS de RPC está habilitado. El proxy IIS de RPC se usa junto con IIS para reenviar las llamadas al mecanismo de RPC desde IIS y es uno de los componentes principales de los servicios de Internet COM, que se habilita estableciendo CISEnabled en true. Para obtener más información sobre RPCProxyEnabled, consulte [seguridad de http RPC](/windows/desktop/Rpc/rpc-over-http-security). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>SecureReferencesEnabled



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Aplica en los equipos DCOM las llamadas entre procesos a los métodos [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) y [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) están protegidos. |
| Access         | ReadWrite                                                                                                                                                                 |
| Tipo           | Bool                                                                                                                                                                      |
| Valor predeterminado        | False                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>SecurityTrackingEnabled



| Entrada | Value |
|----------------|---------------------------------------------------------|
| Descripción    | Establézcalo en true si está habilitado el seguimiento de seguridad en los objetos. |
| Access         | ReadWrite                                               |
| Tipo           | Bool                                                    |
| Valor predeterminado        | True                                                    |
| Sistema mínimo | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina el modo en que la Directiva de restricción de software (SRP) controla las conexiones de activación como activador. Si se establece en true, el nivel de confianza de SRP configurado para el objeto de servidor se compara con el nivel de confianza de SRP del objeto de cliente y se utiliza el nivel de confianza mayor (más riguroso) para ejecutar el objeto de servidor. Si se establece en false, el objeto de servidor se ejecuta con el nivel de confianza de SRP del objeto de cliente, independientemente del nivel de confianza de SRP con el que está configurado el servidor. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Valor predeterminado        | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina la forma en que la Directiva de restricción de software (SRP) controla las conexiones a los procesos existentes. Si se establece en false, los intentos de conexión a objetos en ejecución no se comprueban para los niveles de confianza de SRP correspondientes. Si se establece en true, el objeto que se está ejecutando debe tener un nivel de confianza SRP igual o superior (más estricto) que el objeto de cliente. Por ejemplo, un objeto de cliente con un nivel de confianza SRP sin restricciones no puede conectarse a un objeto en ejecución con un nivel de confianza SRP no permitido. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Valor predeterminado        | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Debe establecerse en un valor suficiente en segundos si realiza numerosas operaciones dentro de una transacción. El período de tiempo de espera predeterminado es de 60 segundos y el período de tiempo de espera máximo es de 3600 segundos (1 hora). Al establecer esta propiedad en 0 se deshabilitan los tiempos de espera de la transacción. Esta propiedad se puede reemplazar por componentes individuales mediante la propiedad ComponentTransactionTimeout de la colección de [**componentes**](components.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Tipo           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Valor predeterminado        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>Ejemplo

En el siguiente ejemplo de Microsoft Visual Basic se muestra cómo conectarse a un equipo remoto y obtener su propiedad SecurityTrackingEnabled mediante la colección **LocalComputer** del equipo remoto. Para usar este ejemplo, agregue la biblioteca de tipos de administración de COM+ como referencia a su proyecto de Visual Basic.


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



Para usar la función, proporcione un valor de cadena para el nombre del equipo remoto. En el siguiente código de Visual Basic se muestra cómo conectarse al equipo denominado "nombreDeEquipoRemoto".


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

 

 
