---
title: Métodos de la propiedad IADsFileShare (iAds. h)
description: Los métodos de propiedad de la interfaz IADsFileshare obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsFileShare ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150772"
---
# <a name="iadsfileshare-property-methods"></a>Métodos de propiedad IADsFileShare

Los métodos de propiedad de la interfaz [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**CurrentUserCount**
</dt> <dd> <dl>

Número de usuarios conectados al recurso compartido.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

**Descripción**
</dt> <dd> <dl>

La descripción del recurso compartido de archivos.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

**HostComputer**
</dt> <dd> <dl>

Una referencia ADsPath al equipo host.

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

**MaxUserCount**
</dt> <dd> <dl>

Número máximo de usuarios con permiso para obtener acceso al recurso compartido al mismo tiempo.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

**Ruta de acceso**
</dt> <dd> <dl>

Ruta de acceso del sistema de archivos al directorio compartido.

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


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Ejemplos

Para tener acceso a las propiedades de los recursos compartidos de archivos de un equipo, primero debe enlazar a "LanmanServer" en el equipo. En el ejemplo de código siguiente se muestra cómo configurar la descripción y el número máximo de usuarios permitidos para todos los recursos compartidos de archivos públicos del equipo, denominados "MiEquipo", en el dominio predeterminado.


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



En el ejemplo de código siguiente se muestra cómo convertir el directorio C: carpetas existente en \\ un recurso compartido de archivos público.


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



En el ejemplo de código siguiente se hace que el directorio C: \\ carpeta de carpetas existente sea un recurso compartido de archivos público.


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsFileShare se define como EB6DCAF0-4B83-11cf-A995-00AA006BC149<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

 





