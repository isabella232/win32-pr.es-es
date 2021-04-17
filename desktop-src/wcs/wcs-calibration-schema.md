---
title: Esquema de calibración de WCS
description: En este tema se describe el esquema de calibración de WCS que expande el perfil de modelo de dispositivo de color WCS.
ms.assetid: 99f3e9e3-15b7-4bca-87cc-a3bf3b6d0112
keywords:
- Sistema de color de Windows (WCS), calibración
- WCS (sistema de colores de Windows), calibración
- Administración del color de imagen, calibración
- Administración del color, calibración
- colores, calibración
- esquemas, calibración
- Calibración WCS
- curva
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e859ab9d2b47355db063961004f17a8cc1537694
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721137"
---
# <a name="wcs-calibration-schema"></a><span data-ttu-id="2fe7f-111">Esquema de calibración de WCS</span><span class="sxs-lookup"><span data-stu-id="2fe7f-111">WCS Calibration Schema</span></span>

<span data-ttu-id="2fe7f-112">En este tema se describe el esquema de calibración de WCS que expande el [Perfil de modelo de dispositivo de color WCS](wcs-color-device-model-profile-schema-and-algorithms.md).</span><span class="sxs-lookup"><span data-stu-id="2fe7f-112">This topic describes the WCS Calibration schema that expands the [WCS color device model profile](wcs-color-device-model-profile-schema-and-algorithms.md).</span></span>

## <a name="the-wcs-calibration-schema"></a><span data-ttu-id="2fe7f-113">El esquema de calibración de WCS</span><span class="sxs-lookup"><span data-stu-id="2fe7f-113">The WCS Calibration Schema</span></span>

<span data-ttu-id="2fe7f-114">La siguiente definición de esquema se usa para especificar las nuevas definiciones de Windows 7 que admiten la calibración del [Perfil del modelo de dispositivo de color WCS](wcs-color-device-model-profile-schema-and-algorithms.md) .</span><span class="sxs-lookup"><span data-stu-id="2fe7f-114">The following schema definition is used to specify the new Windows 7 definitions that support [WCS color device model profile](wcs-color-device-model-profile-schema-and-algorithms.md) calibration.</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<!--
  Copyright (C) Microsoft. All rights reserved. The Windows Color System
  color profile schemas may be used according to the terms of the license agreement
  available at https://www.microsoft.com/whdc/device/display/color/wcs_license.mspx.
  -->
<xs:schema
  xmlns:cal="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model Calibration profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="AdapterGammaConfiguration">
    <xs:choice>
      <xs:element name="ParameterizedCurves" type="wcs:ParameterizedCurvesType"/>
      <xs:element name="HDRToneResponseCurves" type="wcs:HDRToneResponseCurvesType"/>
    </xs:choice>
  </xs:complexType>

  <xs:complexType name="Calibration">
    <xs:sequence>
      <xs:element name="AdapterGammaConfiguration" type="cal:AdapterGammaConfiguration" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>

</xs:schema>
```



<span data-ttu-id="2fe7f-115">Por compatibilidad con Windows Vista, los perfiles que contienen etiquetas de calibración deben incluir el atributo `mc:Ignoreable="cdm_calibration"` .</span><span class="sxs-lookup"><span data-stu-id="2fe7f-115">For compatibility with Windows Vista, profiles containing calibration tags should include the attribute `mc:Ignoreable="cdm_calibration"`.</span></span>

 

 




