---
description: Proporciona acceso al contexto de un objeto CAPICOM X.509v3 Certificate. Este contexto permite usar el certificado CAPICOM en otras derivaciones de CryptoAPI.
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
ms.openlocfilehash: 693e259c730209049f669d1499001d026b3d11088c7bef09616826a4673cac0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006043"
---
# <a name="icertcontext-interface"></a>Interfaz ICertContext

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La **interfaz ICertContext** proporciona acceso al contexto de un objeto CAPICOM X.509v3 [**Certificate.**](certificate.md) Este contexto permite usar el certificado CAPICOM en otras derivaciones de CryptoAPI.

## <a name="when-to-use"></a>Cuándo se usa

Use esta interfaz cuando necesite usar [](certificate.md) un objeto de certificado CAPICOM en otra derivación de CryptoAPI.

## <a name="members"></a>Miembros

La **interfaz ICertContext** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz ICertContext** tiene estos métodos.



| Método                                          | Descripción                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](icertcontext-freecontext.md) | Libera un CONTEXTO DE PCCERT \_ adquirido a través de la propiedad [**CertContext.**](icertcontext-certcontext.md)<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz ICertContext** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso           | Descripción                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**CertContext**](icertcontext-certcontext.md)<br/> | Lectura/escritura<br/> | Establece o recupera el contexto de PCCERT \_ de un certificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




