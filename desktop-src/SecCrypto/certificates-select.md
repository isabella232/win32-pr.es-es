---
description: Muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de los certificados seleccionados.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'ICertificates2:: SELECT (método)'
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
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691019"
---
# <a name="icertificates2select-method"></a>ICertificates2:: SELECT (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Select** muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de los certificados seleccionados. Este método se presentó en CAPICOM 2,0.

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

*Título* \[ de en, opcional\]
</dt> <dd>

Cadena que contiene el título del cuadro de diálogo. El valor predeterminado es una cadena vacía ("").

</dd> <dt>

*DisplayString* \[ en, opcional\]
</dt> <dd>

Cadena que contiene el texto del mensaje que se muestra con el cuadro de diálogo. El valor predeterminado es una cadena vacía ("").

</dd> <dt>

*bMultiSelect* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si el usuario puede seleccionar más de un certificado. True indica que se pueden seleccionar varios certificados mediante la tecla CTRL o Mayús. El valor predeterminado es false.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto de [**certificados**](certificates.md) que contiene los certificados seleccionados en el cuadro de diálogo.

**CAPICOM 2,1:** El objeto de [**certificados**](certificates.md) que se devuelve contiene referencias a los certificados de la colección de la que se realizó la selección. Cualquier cambio realizado en los certificados del objeto de **certificados** devueltos se refleja en esa colección.

**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 y CAPICOM 2.0.0.3:** El objeto de [**certificados**](certificates.md) que se devuelve contiene copias de los certificados de la colección de la que se realizó la selección. Los cambios realizados en los certificados del objeto de **certificados** devueltos no se reflejan en esa colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
