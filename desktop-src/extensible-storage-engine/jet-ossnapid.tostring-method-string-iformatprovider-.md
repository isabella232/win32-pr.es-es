---
description: 'Más información sobre: JET_OSSNAPID. Método ToString (String, IFormatProvider)'
title: JET_OSSNAPID. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512151
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 56e86765839434f2cd3a67c18f6395dd5443f21f8b905e6f86e6e85ad9915c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038873"
---
# <a name="jet_ossnapidtostring-method-string-iformatprovider"></a>JET_OSSNAPID. Método ToString (String, IFormatProvider)

Da formato al valor de la instancia actual usando el formato especificado.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_OSSNAPID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a>Parámetros

  - format  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Cadena [que](/dotnet/api/system.string) especifica el formato que se usará. -o bien- null para usar el formato predeterminado definido para el tipo de implementación [de IFormattable.](/dotnet/api/system.iformattable)

<!-- end list -->

  - formatProvider  
    Tipo: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    [IFormatProvider que se](/dotnet/api/system.iformatprovider) usará para dar formato al valor. -o bien- null para obtener la información de formato numérico de la configuración regional actual del sistema operativo.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.String](/dotnet/api/system.string)  
Cadena [que](/dotnet/api/system.string) contiene el valor de la instancia actual en el formato especificado.  

#### <a name="implements"></a>Implementaciones

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_OSSNAPID estructura](./jet-ossnapid-structure.md)

[JET_OSSNAPID miembros](./jet-ossnapid-members.md)

[Sobrecarga de ToString](./jet-ossnapid.tostring-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
