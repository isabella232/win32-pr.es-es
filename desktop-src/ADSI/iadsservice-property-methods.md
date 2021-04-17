---
title: Métodos de la propiedad IADsService (iAds. h)
description: Lea y escriba las propiedades descritas en este tema.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsService ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656529"
---
# <a name="iadsservice-property-methods"></a>Métodos de propiedad IADsService

Los métodos de propiedad de la interfaz [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) leen y escriben las propiedades descritas en este tema. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Dependencias**
</dt> <dd> <dl>

Matriz de nombres **BSTR** de servicios o grupos de carga que se deben cargar para que este servicio pueda cargarse. La sintaxis de la entrada es "Service:" seguida del nombre del servicio o "Group:" seguido del nombre del grupo de carga.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

**DisplayName**
</dt> <dd> <dl>

Nombre descriptivo del servicio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

**ErrorControl**
</dt> <dd> <dl>

Acción que se va a realizar si se produce un error en el inicio de este servicio. Los valores siguientes son válidos para esta propiedad.

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>ERROR del servicio ADS- \_ \_ \_ omitir * * * *


</dt> <dd>

El programa de inicio registra el error, pero continúa con la operación de inicio.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\_error del servicio ADS \_ \_ normal * * * *


</dt> <dd>

El programa de inicio registra el error y presenta un cuadro de mensaje, pero continúa con la operación de inicio.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_error grave del servicio ADS \_ \_ * * * *


</dt> <dd>

El programa de inicio registra el error. Si se inicia la última configuración válida conocida, la operación de inicio continúa. De lo contrario, el sistema se reinicia con la última configuración válida conocida.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_error del servicio ADS \_ \_ crítico * * * *


</dt> <dd>

Si es posible, el programa de inicio registra el error. Si se está iniciando la última configuración válida conocida, se produce un error en la operación de inicio. De lo contrario, el sistema se reinicia con la última configuración válida conocida.

</dd> </dl> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

**HostComputer**
</dt> <dd> <dl>

Cadena ADsPath del host de este servicio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

**LoadOrderGroup**
</dt> <dd> <dl>

Nombre del grupo de orden de carga al que pertenece este servicio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

**Ruta de acceso**
</dt> <dd> <dl>

Ruta de acceso y nombre de archivo del archivo ejecutable de este servicio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountName**
</dt> <dd> <dl>

Nombre de la cuenta que usa este servicio para autenticarse en el inicio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountPath**
</dt> <dd> <dl>

Ruta de acceso de la cuenta especificada por la propiedad **ServiceAccountPath** .

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

**ServiceType**
</dt> <dd> <dl>

La descripción de cómo se presenta un servicio en el equipo host. Esta propiedad puede ser cero o una combinación de uno o varios de los valores siguientes.

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

\_Controlador de kernel del servicio ADS * * * * \_ \_ (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

\_ \_ Controlador del sistema de archivos del servicio ADS * * * * \_ \_ (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

\_ \_ Proceso propio del servicio ADS \_ * * * * (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

Proceso de recurso compartido de servicio de ADS * * * * \_ \_ \_ (0x00000020)


</dt> <dd></dd> </dl> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

**StartType**
</dt> <dd> <dl>

Determina cómo iniciar el servicio. Los valores siguientes son válidos para esta propiedad.

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\_Inicio de arranque del servicio ADS \_ \_ * * * *


</dt> <dd>

El servicio es un controlador de dispositivo Iniciado por el cargador del sistema. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_ \_ Inicio del sistema de servicio ADS \_ * * * *


</dt> <dd>

El servicio es un controlador de dispositivo Iniciado por la función **IoInitSystem** . Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_Inicio automático del servicio ADS \_ \_ * * * *


</dt> <dd>

El administrador de control de servicios iniciará automáticamente el servicio durante el inicio del sistema.

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>Inicio de la \_ demanda del servicio ADS \_ \_ * * * *


</dt> <dd>

El administrador de control de servicios iniciará el servicio cuando un proceso llame a la función [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_servicio ADS \_ deshabilitado * * * *


</dt> <dd>

No se puede iniciar el servicio. Intenta iniciar el resultado del servicio en el servicio de error de código de error **\_ \_ deshabilitado**.

</dd> </dl> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

**StartupParameters**
</dt> <dd> <dl>

Parámetros pasados al servicio en el inicio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

**Versión**
</dt> <dd> <dl>

Versión del servicio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo enumerar todos los servicios del sistema disponibles que se ejecutan en el equipo host, "MiEquipo", junto con la ubicación para buscar los ejecutables de los servicios.


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsService se define como 68AF66E0-31CA-11cf-A98A-00AA006BC149<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

