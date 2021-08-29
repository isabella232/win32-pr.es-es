---
title: Uso de un ActiveX de datos para enlazar a proveedores ADSI
description: Dado que ADSI también es un OLE DB, puede usar un objeto ActiveX data (ADO) para conectarse a los proveedores adsi.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX ADSI del objeto de datos
- ActiveX adsi del objeto de datos , mediante ADO para enlazar a proveedores adsi
- ADSI de proveedores de servicios, ActiveX objeto de datos al que enlazar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c34e026fabe34e52bcfbd9182cca935cf7e019b1fd1c3c8f97fd2f88be48c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637535"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>Uso de un ActiveX de datos para enlazar a proveedores ADSI

Dado que ADSI también es un OLE DB, puede usar un objeto ActiveX data (ADO) para conectarse a los proveedores adsi. Al igual que con otros proveedores de ADO, para conectarse a un proveedor de OLE DB, debe crear un nuevo objeto de conexión y, opcionalmente, especificar las credenciales. El nombre del proveedor de OLE DB ADSI **es ADsDSOObject**.

Por ejemplo:


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



En el ejemplo anterior, está conectado en nombre del usuario actual. Para especificar credenciales diferentes, use las propiedades de conexión:


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



AdsI OLE DB define las siguientes propiedades de conexión.



| Propiedad           | Tipo de datos   | Valor predeterminado   |
|--------------------|-------------|-----------|
| "Id. de usuario"          | **Bstr**    | **NULL**  |
| "Password"         | **Bstr**    | **NULL**  |
| "Cifrar contraseña" | **Booleana** | **FALSE** |
| "Marca ADSI"        | **Long**    | 0         |



 

Con OLE DB ADO, no se puede enlazar a un objeto específico. Sin embargo, puede consultar un objeto específico y obtener un conjunto de resultados. Solo los proveedores adsi que [**admiten IDirectorySearch se**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) benefician de tener ADO como modelo de programación.

La propiedad ADSI Flag se usa para especificar la opción de autenticación de enlace. Esta propiedad puede ser una combinación de marcas de la [**enumeración ADS \_ AUTHENTICATION \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)

 

 




