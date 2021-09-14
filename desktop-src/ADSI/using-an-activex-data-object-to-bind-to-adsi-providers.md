---
title: Usar un objeto ActiveX datos para enlazar a proveedores ADSI
description: Como ADSI también es un proveedor OLE DB, puede usar un ActiveX Data Object (ADO) para conectarse a proveedores adsi.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX ADSI del objeto de datos
- ActiveX adsi del objeto de datos , mediante ADO para enlazar a proveedores adsi
- ADSI de proveedores de servicios, ActiveX objeto de datos al que enlazar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970396"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>Usar un objeto ActiveX datos para enlazar a proveedores ADSI

Como ADSI también es un proveedor OLE DB, puede usar un ActiveX Data Object (ADO) para conectarse a proveedores adsi. Al igual que con otros proveedores de ADO, para conectarse a un proveedor de OLE DB, debe crear un nuevo objeto de conexión y, opcionalmente, especificar las credenciales. El nombre del proveedor de OLE DB ADSI es **ADsDSOObject**.

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



ADSI OLE DB define las siguientes propiedades de conexión.



| Propiedad           | Tipo de datos   | Valor predeterminado   |
|--------------------|-------------|-----------|
| "Id. de usuario"          | **BSTR**    | **NULL**  |
| "Password"         | **BSTR**    | **NULL**  |
| "Cifrar contraseña" | **BOOLEANA** | **FALSE** |
| "AdsI Flag"        | **Long**    | 0         |



 

Con OLE DB ADO, no se puede enlazar a un objeto específico. Sin embargo, puede consultar un objeto específico y obtener un conjunto de resultados. Solo los proveedores adsi que [**admiten IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se benefician de tener ADO como modelo de programación.

La propiedad ADSI Flag se usa para especificar la opción de autenticación de enlace. Esta propiedad puede ser una combinación de marcas de la [**enumeración ADS \_ AUTHENTICATION \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)

 

 




