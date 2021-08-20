---
description: Muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de esos certificados seleccionados.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: ICertificates2::Select (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 50e10a9487318c7b89e89afb3d10d5974524c821b76618ca8ffd1f282e844f65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770490"
---
# <a name="icertificates2select-method"></a>ICertificates2::Select (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Select** muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de esos certificados seleccionados. Este método se introdujo en CAPICOM 2.0.

## <a name="syntax"></a>Sintaxis


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Título* \[ en, opcional\]
</dt> <dd>

Cadena que contiene el título del cuadro de diálogo. El valor predeterminado es una cadena vacía ("").

</dd> <dt>

*DisplayString* \[ en, opcional\]
</dt> <dd>

Cadena que contiene el texto del aviso que se muestra con el cuadro de diálogo. El valor predeterminado es una cadena vacía ("").

</dd> <dt>

*bMultiSelect* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si el usuario puede seleccionar más de un certificado. True indica que se pueden seleccionar varios certificados mediante la tecla CTRL o MAYÚS. El valor predeterminado es false.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**Certificates**](certificates.md) que contiene los certificados seleccionados en el cuadro de diálogo.

**CAPICOM 2.1:** El [**objeto Certificates**](certificates.md) que se devuelve contiene referencias a los certificados de la colección desde la que se realizó la selección. Los cambios realizados en los certificados en el **objeto Certificates** devuelto se reflejan en esa colección.

**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 y CAPICOM 2.0.0.3:** El [**objeto Certificates**](certificates.md) que se devuelve contiene copias de los certificados de la colección desde la que se realizó la selección. Los cambios realizados en los certificados en el **objeto Certificates** devuelto no se reflejan en esa colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
