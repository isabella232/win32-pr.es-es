---
title: Interfaz IMsTscNonScriptable
description: Contiene propiedades y métodos relacionados con la aplicación de una contraseña al control Escritorio remoto ActiveX datos.
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- Interfaz IMsTscNonScriptable Servicios de Escritorio remoto
- Interfaz IMsTscNonScriptable Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsTscNonScriptable
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ce3b1e921635850e9ffa713c55a812a806ac4e757e772569e7db817410ad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770655"
---
# <a name="imstscnonscriptable-interface"></a>Interfaz IMsTscNonScriptable

Contiene propiedades y métodos relacionados con la aplicación de una contraseña al control Escritorio remoto ActiveX datos.

El uso principal de la interfaz **IMsTscNonScriptable** es configurar el acceso de inicio de sesión de contraseña automático a servidores de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) en escenarios donde el control Escritorio remoto ActiveX se hospeda en un contenedor escrito de forma personalizada. Cuando se configura el inicio de sesión automático, el usuario no recibe el cuadro de diálogo Windows inicio de sesión en el momento de la conexión.

En algunas plataformas, los métodos de la **interfaz IMsTscNonScriptable** se pueden usar para especificar contraseñas en uno de los tres formatos admitidos:

-   Texto no cifrado
-   Codificación portable
-   Binario (noportable) codificado

Tenga en cuenta que una contraseña en un formato codificado consta de dos partes:

-   Parte de contraseña codificada.
-   Elemento de valor sal.

Ambas partes son necesarias para establecer una contraseña codificada. Ni la parte de contraseña codificada ni la parte de valor sal deben considerarse cifradas de forma segura.

El acceso mediante script a las contraseñas de texto no cifrado está disponible a través de la [**propiedad ClearTextPassword**](imsrdpclientadvancedsettings-cleartextpassword.md) de la interfaz que acepta scripts [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).

Solo se puede acceder a la interfaz **IMsTscNonScriptable** a través de la tabla virtual.

## <a name="members"></a>Miembros

La **interfaz IMsTscNonScriptable** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsTscNonScriptable** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IMsTscNonScriptable** tiene estos métodos.



| Método                                                     | Descripción                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**ResetPassword**](imstscnonscriptable-resetpassword.md) | Restablece todos los estados de contraseña del control .<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IMsTscNonScriptable** tiene estas propiedades.



| Propiedad                                                                      | Tipo de acceso           | Descripción                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>       | Lectura/escritura<br/> | Esta propiedad no es compatible.<br/>                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>               | Lectura/escritura<br/> | Esta propiedad no es compatible.<br/>                                   |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/> | Solo escritura<br/> | El Escritorio remoto ActiveX contraseña de control, en formato de texto no cifrado.<br/> |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>   | Lectura/escritura<br/> | Esta propiedad no es compatible.<br/>                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>           | Lectura/escritura<br/> | Esta propiedad no es compatible.<br/>                                   |



 

## <a name="remarks"></a>Comentarios

Proporcionar una contraseña al control Escritorio remoto ActiveX es opcional. Si proporciona una contraseña al control, debe aplicar solo uno de los tres formatos anteriores al control antes de iniciar la conexión con una llamada al método [**Conectar.**](imstscax-connect.md)

> [!Note]  
> También puede habilitar el inicio de sesión automático en el servidor con la herramienta de configuración de Servicios de Escritorio remoto (Tscc.msc). Un administrador puede usar esta herramienta para asignar una contraseña específica a una conexión en una situación en la que se necesita un inicio de sesión automatizado.

 

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

Las interfaces siguientes han ampliado la interfaz **IMsTscNonScriptable,** donde cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID MsRdpClient se define como \_ 791fa017-2de3-492e-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient2 se define como \_ 9059F30F-4EB1-4BD2-9FDC-36F43A218F4A<br/> CLSID \_ MsRdpClient2a se define como 971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting se define como 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID \_ MsRdpClient3 se define como 7584C670-2274-4EFB-B00B-D6AABA6D3850<br/> CLSID \_ MsRdpClient3a se define como 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting se define como ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID MsRdpClient4 se define como \_ 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a se define como 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting se define como 6AE29350-321B-42BE- JAVASCRIPT5-12FB5270C0DE<br/> CLSID MsRdpClient5 se define como \_ 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting se define como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID MsRdpClient6 se define como \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID MsRdpClient7 se define como \_ A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 se define como \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting se define como 7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> CLSID MsTscAx se define como \_ 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting se define como A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsTscNonScriptable se define como C1E6743A-41C1-4A74-832A-0DD06C1C7A0E<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAx::Conectar**](imstscax-connect.md)
</dt> </dl>

 

