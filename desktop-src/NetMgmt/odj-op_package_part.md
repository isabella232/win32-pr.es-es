---
title: OP_PACKAGE_PART
description: OP_PACKAGE_PART definición de IDL
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566893"
---
# <a name="op_package_part-structure"></a>OP_PACKAGE_PART estructura

Define una estructura que contiene un conjunto de datos identificado por un GUID.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a>Members

### <a name="parttype"></a>PartType

Identifica la estructura serializada contenida en Part según la tabla siguiente:

|PartType|Significado|
| --- | --- |
|GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}|Contiene una estructura ODJ_WIN7_BLOB serializada.|
|GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}|Contiene una estructura OP_JOIN_PROV2_PART serializada.|
|GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}|Contiene una estructura OP_JOIN_PROV3_PART serializada.|
|GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}|Contiene una estructura OP_CERT_PART serializada.|
|GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}|Contiene una estructura OP_POLICY_PART serializada.|

### <a name="ulflags"></a>ulFlags

Debe establecerse en cero o más de las marcas siguientes:

|Value|Significado|
| --- | --- |
|OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)|Esta parte del paquete se considera esencial. Si el consumidor no reconoce esta parte del paquete o no lo procesa correctamente, se debe producir un error en la operación general.|

### <a name="part"></a>Parte

Contiene una estructura serializada en una OP_BLOB estructura. PartType determina la estructura específica.

### <a name="extension"></a>Extensión

Reservado para uso futuro y DEBE establecerse en todos los ceros.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**BLOB DE \_ OPERACIÓN**](odj-op_blob.md)
