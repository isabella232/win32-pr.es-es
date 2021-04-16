---
description: Proporciona acceso al contexto de un objeto de certificado de CAPICOM X. 509v3. Este contexto permite usar el certificado de CAPICOM en otras derivaciones de CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Interfaz ICertContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671619"
---
# <a name="icertcontext-interface"></a>Interfaz ICertContext

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La interfaz **ICertContext** proporciona acceso al contexto de un objeto de [**certificado**](certificate.md) de CAPICOM X. 509v3. Este contexto permite usar el certificado de CAPICOM en otras derivaciones de CryptoAPI.

## <a name="when-to-use"></a>Cuándo se usa

Use esta interfaz cuando necesite usar un objeto de [**certificado**](certificate.md) de CAPICOM en otra derivación de CryptoAPI.

## <a name="members"></a>Miembros

La interfaz **ICertContext** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **ICertContext** tiene estos métodos.



| Método                                          | Descripción                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](icertcontext-freecontext.md) | Libera un \_ contexto PCCERT adquirido a través de la propiedad [**CertContext**](icertcontext-certcontext.md) .<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **ICertContext** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso           | Descripción                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**CertContext**](icertcontext-certcontext.md)<br/> | Lectura/escritura<br/> | Establece o recupera el contexto PCCERT \_ de un certificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




