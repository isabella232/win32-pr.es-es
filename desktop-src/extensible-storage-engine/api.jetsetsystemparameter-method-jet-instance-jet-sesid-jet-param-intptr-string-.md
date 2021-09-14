---
description: 'Más información sobre: Método Api.JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)'
title: Método Api.JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100822
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a92ea3d6b6d4b828e409cd08b896f54c4aa053
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969451"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string"></a>Método Api.JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)

Establece las opciones de configuración de la base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As IntPtr, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    IntPtr paramValue,
    string paramString
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia en la que se establece la opción o [Nil para](./jet-instance.nil-property.md) establecer la opción en todas las instancias.

<!-- end list -->

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - paramid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)  
    
    Parámetro que se establecerá.

<!-- end list -->

  - paramValue  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Valor del parámetro que se va a establecer, si el parámetro es un tipo entero.

<!-- end list -->

  - paramString  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Valor del parámetro que se va a establecer, si el parámetro es un tipo de cadena.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Código de advertencia de ESENT.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetSetSystemParameter](./api.jetsetsystemparameter-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
