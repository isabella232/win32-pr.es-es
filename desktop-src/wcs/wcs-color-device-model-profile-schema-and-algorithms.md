---
title: Algoritmos y esquema de perfil del modelo de dispositivo de color de WCS
description: En este tema se proporciona información sobre el esquema de Perfil de modelo de dispositivo de color WCS y sus algoritmos asociados. Este tema contiene las siguientes secciones OverviewColor Device Model Profile ArchitectureThe CDMP SchemaWCS CDMP v 2.0 Calibration AdditionThe CDMP Schema ElementsColorDeviceModelProfileColorDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCMYKPrinterDevice elementRGBVirtualDevice elementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTy peMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe CDMP Baseline AlgorithmsCRT Device Model BaselineLCD modelo de dispositivo de impresora BaselineRGB modelo de dispositivo virtual BaselineRGB modelo de dispositivo de impresora BaselineCMYK proyector modelo de dispositivo BaselineRGB
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Sistema de color de Windows (WCS), perfil de modelo de dispositivo de color (CDMP)
- WCS (sistema de color de Windows), perfil de modelo de dispositivo de color (CDMP)
- Administración del color de imagen, perfil de modelo de dispositivo de color (CDMP)
- Administración del color, perfil de modelo de dispositivo de color (CDMP)
- colores, perfil de modelo de dispositivo de color (CDMP)
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- esquemas, perfil de modelo de dispositivo de color (CDMP)
- algoritmos, perfil de modelo de dispositivo de color (CDMP)
- Perfil de modelo de dispositivo de color (CDMP)
- CDMP (Perfil de modelo de dispositivo de color)
- Perfil de modelo de dispositivo de color WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b671bf97625b00c99060e65be4d39c44e5b35f
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554085"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a><span data-ttu-id="3d502-118">Algoritmos y esquema de perfil del modelo de dispositivo de color de WCS</span><span class="sxs-lookup"><span data-stu-id="3d502-118">WCS Color Device Model Profile Schema and Algorithms</span></span>

<span data-ttu-id="3d502-119">En este tema se proporciona información sobre el esquema de Perfil de modelo de dispositivo de color WCS y sus algoritmos asociados.</span><span class="sxs-lookup"><span data-stu-id="3d502-119">This topic provides information about the WCS Color Device Model Profile Schema and its associated algorithms.</span></span>

<span data-ttu-id="3d502-120">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="3d502-120">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3d502-121">Información general</span><span class="sxs-lookup"><span data-stu-id="3d502-121">Overview</span></span>](#overview)
-   [<span data-ttu-id="3d502-122">Arquitectura de Perfil de modelo de dispositivo de color</span><span class="sxs-lookup"><span data-stu-id="3d502-122">Color Device Model Profile Architecture</span></span>](#color-device-model-profile-architecture)
-   [<span data-ttu-id="3d502-123">El esquema CDMP</span><span class="sxs-lookup"><span data-stu-id="3d502-123">The CDMP Schema</span></span>](#the-cdmp-schema)
-   [<span data-ttu-id="3d502-124">Adición de calibración de CDMP v 2.0 de WCS</span><span class="sxs-lookup"><span data-stu-id="3d502-124">WCS CDMP v2.0 Calibration Addition</span></span>](#wcs-cdmp-v20-calibration-addition)
-   [<span data-ttu-id="3d502-125">Los elementos de esquema CDMP</span><span class="sxs-lookup"><span data-stu-id="3d502-125">The CDMP Schema Elements</span></span>](#the-cdmp-schema-elements)
    -   [<span data-ttu-id="3d502-126">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="3d502-126">ColorDeviceModelProfile</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="3d502-127">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="3d502-127">ColorDeviceModel</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="3d502-128">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="3d502-128">NamespaceVersion</span></span>](#namespaceversion)
    -   [<span data-ttu-id="3d502-129">Versión</span><span class="sxs-lookup"><span data-stu-id="3d502-129">Version</span></span>](#namespaceversion)
    -   [<span data-ttu-id="3d502-130">Documentación</span><span class="sxs-lookup"><span data-stu-id="3d502-130">Documentation</span></span>](#documentation)
    -   [<span data-ttu-id="3d502-131">Elemento CRTDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-131">CRTDevice element</span></span>](#crtdevice-element)
    -   [<span data-ttu-id="3d502-132">Elemento LCDDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-132">LCDDevice element</span></span>](#lcddevice-element)
    -   [<span data-ttu-id="3d502-133">Elemento ProjectorDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-133">ProjectorDevice element</span></span>](#projectordevice-element)
    -   [<span data-ttu-id="3d502-134">Elemento ScannerDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-134">ScannerDevice element</span></span>](#scannerdevice-element)
    -   [<span data-ttu-id="3d502-135">Elemento CameraDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-135">CameraDevice element</span></span>](#cameradevice-element)
    -   [<span data-ttu-id="3d502-136">Elemento RGBPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-136">RGBPrinterDevice element</span></span>](#rgbprinterdevice-element)
    -   [<span data-ttu-id="3d502-137">Elemento CMYKPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-137">CMYKPrinterDevice element</span></span>](#cmykprinterdevice-element)
    -   [<span data-ttu-id="3d502-138">Elemento RGBVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-138">RGBVirtualDevice element</span></span>](#rgbvirtualdevice-element)
    -   [<span data-ttu-id="3d502-139">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="3d502-139">PlugInDeviceType</span></span>](#plugindevicetype)
    -   [<span data-ttu-id="3d502-140">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-140">RGBVirtualMeasurementType</span></span>](#rgbvirtualmeasurementtype)
    -   [<span data-ttu-id="3d502-141">GammaType</span><span class="sxs-lookup"><span data-stu-id="3d502-141">GammaType</span></span>](#gammatype)
    -   [<span data-ttu-id="3d502-142">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="3d502-142">GammaOffsetGainType</span></span>](#gammaoffsetgaintype)
    -   [<span data-ttu-id="3d502-143">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="3d502-143">GammaOffsetGainLinearGainType</span></span>](#gammaoffsetgainlineargaintype)
    -   [<span data-ttu-id="3d502-144">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="3d502-144">ToneResponseCurvesType</span></span>](#toneresponsecurvestype)
    -   [<span data-ttu-id="3d502-145">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="3d502-145">GamutBoundarySamplesType</span></span>](#gamutboundarysamplestype)
    -   [<span data-ttu-id="3d502-146">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="3d502-146">FloatPairList</span></span>](#floatpairlist)
    -   [<span data-ttu-id="3d502-147">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-147">CMYKPrinterMeasurementType</span></span>](#cmykprintermeasurementtype)
    -   [<span data-ttu-id="3d502-148">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-148">RGBPrinterMeasurementType</span></span>](#rgbprintermeasurementtype)
    -   [<span data-ttu-id="3d502-149">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-149">RGBCaptureMeasurementType</span></span>](#rgbcapturemeasurementtype)
    -   [<span data-ttu-id="3d502-150">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="3d502-150">OneBasedIndex</span></span>](#onebasedindex)
    -   [<span data-ttu-id="3d502-151">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-151">RGBProjectorMeasurementType</span></span>](#rgbprojectormeasurementtype)
    -   [<span data-ttu-id="3d502-152">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-152">DisplayMeasurementType</span></span>](#displaymeasurementtype)
    -   [<span data-ttu-id="3d502-153">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="3d502-153">MeasurementConditionsType</span></span>](#measurementconditionstype)
    -   [<span data-ttu-id="3d502-154">GeometryType</span><span class="sxs-lookup"><span data-stu-id="3d502-154">GeometryType</span></span>](#geometrytype)
    -   [<span data-ttu-id="3d502-155">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="3d502-155">RGBPrimariesGroup</span></span>](#rgbprimariesgroup)
    -   [<span data-ttu-id="3d502-156">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="3d502-156">NonNegativeCMYKSampleType</span></span>](#nonnegativecmyksampletype)
    -   [<span data-ttu-id="3d502-157">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="3d502-157">NonNegativeRGBSampleType</span></span>](#nonnegativergbsampletype)
    -   [<span data-ttu-id="3d502-158">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="3d502-158">NonNegativeCMYKType</span></span>](#nonnegativecmyktype)
    -   [<span data-ttu-id="3d502-159">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="3d502-159">NonNegativeRGBType</span></span>](#nonnegativergbtype)
    -   [<span data-ttu-id="3d502-160">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="3d502-160">ExtensionType</span></span>](#extensiontype)
    -   [<span data-ttu-id="3d502-161">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-161">NonNegativeXYZType</span></span>](#nonnegativexyztype)
    -   [<span data-ttu-id="3d502-162">XYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-162">XYZType</span></span>](#nonnegativexyztype)
-   [<span data-ttu-id="3d502-163">Algoritmos de línea de base de CDMP</span><span class="sxs-lookup"><span data-stu-id="3d502-163">The CDMP Baseline Algorithms</span></span>](#the-cdmp-baseline-algorithms)
    -   [<span data-ttu-id="3d502-164">Línea de base del modelo de dispositivo CRT</span><span class="sxs-lookup"><span data-stu-id="3d502-164">CRT Device Model Baseline</span></span>](#crt-device-model-baseline)
    -   [<span data-ttu-id="3d502-165">Línea de base del modelo de dispositivo LCD</span><span class="sxs-lookup"><span data-stu-id="3d502-165">LCD Device Model Baseline</span></span>](#lcd-device-model-baseline)
    -   [<span data-ttu-id="3d502-166">Línea base del modelo de dispositivo de impresora RGB</span><span class="sxs-lookup"><span data-stu-id="3d502-166">RGB Printer Device Model Baseline</span></span>](#rgb-printer-device-model-baseline)
    -   [<span data-ttu-id="3d502-167">Línea base de modelo de dispositivo virtual RGB</span><span class="sxs-lookup"><span data-stu-id="3d502-167">RGB Virtual Device Model Baseline</span></span>](#rgb-virtual-device-model-baseline)
    -   [<span data-ttu-id="3d502-168">Línea de base del modelo de dispositivo de impresora CMYK</span><span class="sxs-lookup"><span data-stu-id="3d502-168">CMYK Printer Device Model Baseline</span></span>](#cmyk-printer-device-model-baseline)
    -   [<span data-ttu-id="3d502-169">Línea de base del modelo de dispositivo de proyector RGB</span><span class="sxs-lookup"><span data-stu-id="3d502-169">RGB Projector Device Model Baseline</span></span>](#rgb-projector-device-model-baseline)
    -   [<span data-ttu-id="3d502-170">Línea de base del modelo de dispositivo ICC</span><span class="sxs-lookup"><span data-stu-id="3d502-170">ICC Device Model Baseline</span></span>](#icc-device-model-baseline)
-   [<span data-ttu-id="3d502-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d502-171">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="3d502-172">Información general</span><span class="sxs-lookup"><span data-stu-id="3d502-172">Overview</span></span>

<span data-ttu-id="3d502-173">Este esquema se utiliza para especificar el contenido de un perfil de modelo de dispositivo de color (CDMP).</span><span class="sxs-lookup"><span data-stu-id="3d502-173">This schema is used to specify the content of a color device model profile(CDMP).</span></span> <span data-ttu-id="3d502-174">A continuación se describen los algoritmos de línea de base asociados.</span><span class="sxs-lookup"><span data-stu-id="3d502-174">The associated baseline algorithms are described below.</span></span>

<span data-ttu-id="3d502-175">El esquema de Perfil de modelo de dispositivo básico (DMP) consta de los datos de medición de muestreo.</span><span class="sxs-lookup"><span data-stu-id="3d502-175">The basic device model profile (DMP) schema consists of the sampling measurement data.</span></span>

<span data-ttu-id="3d502-176">El componente de muestreo del esquema XML de DMP proporciona compatibilidad con los objetivos básicos de medición de color, centrándose en los destinos estándar comunes y los destinos optimizados para los modelos de dispositivo de línea de base.</span><span class="sxs-lookup"><span data-stu-id="3d502-176">The sampling component of the DMP XML schema provides support for basic color measurement targets, focusing on common standard targets and targets optimized for the baseline device models.</span></span>

<span data-ttu-id="3d502-177">Además, el perfil de dispositivo proporciona información específica sobre el modelo de dispositivo de destino y proporciona una directiva que el modelo de dispositivo de reserva de línea de base puede usar si el modelo de destino no está disponible.</span><span class="sxs-lookup"><span data-stu-id="3d502-177">In addition, the device profile provides specific information on the targeted device model and provides a policy that the baseline fallback device model can use if the targeted model is unavailable.</span></span> <span data-ttu-id="3d502-178">Las instancias de perfil pueden incluir extensiones privadas mediante mecanismos de extensión XML estándar.</span><span class="sxs-lookup"><span data-stu-id="3d502-178">The profile instances can include private extensions using standard XML extension mechanisms.</span></span>

## <a name="color-device-model-profile-architecture"></a><span data-ttu-id="3d502-179">Arquitectura de Perfil de modelo de dispositivo de color</span><span class="sxs-lookup"><span data-stu-id="3d502-179">Color Device Model Profile Architecture</span></span>

![Diagrama que muestra la información que constituye un perfil de modelo de dispositivo.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a><span data-ttu-id="3d502-181">El esquema CDMP</span><span class="sxs-lookup"><span data-stu-id="3d502-181">The CDMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="RGBType">
    <xs:attribute name="R" type="xs:float" use="required"/>
    <xs:attribute name="G" type="xs:float" use="required"/>
    <xs:attribute name="B" type="xs:float" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeRGBType">
    <xs:attribute name="R" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="G" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="B" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeCMYKType">
    <xs:attribute name="C" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="M" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="K" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeRGBSampleType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:NonNegativeRGBType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeCMYKSampleType">
    <xs:sequence>
      <xs:element name="CMYK" type="cdm:NonNegativeCMYKType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:group name="RGBPrimariesGroup">
    <xs:sequence>
      <xs:element name="WhitePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="RedPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="GreenPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BluePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BlackPrimary" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
  </xs:group> 
  
  <xs:complexType name="MeasurementConditionsType">
    <xs:annotation>
      <xs:documentation>
      Optional measurement conditions. 
       
      We only support CIEXYZ for measurement color space in this version. 
      If the white point value from the measurement conditions is not available, 
      the default processing will use
        - "D50" for printer and scanners
        - "D65" for camera and displays.          
      </xs:documentation>
    </xs:annotation>
    <xs:sequence>
      <xs:element name="ColorSpace" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="CIEXYZ"/>
          </xs:restriction>
        </xs:simpleType>    
      </xs:element>
      <xs:choice minOccurs="0">
        <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
        <xs:element name="WhitePointName">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="D50"/>
              <xs:enumeration value="D65"/>
              <xs:enumeration value="A"/>
              <xs:enumeration value="F2"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:choice>
      <xs:element name="Geometry" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="0/45"/>
            <xs:enumeration value="0/diffuse"/>
            <xs:enumeration value="diffuse/0"/>
            <xs:enumeration value="direct"/>
          </xs:restriction>
        </xs:simpleType>   
      </xs:element>
      <xs:element name="ApertureSize" type="xs:int" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="DisplayMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="GrayRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="RedRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GreenRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="BlueRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBProjectorMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:simpleType name="OneBasedIndex">
    <xs:restriction base="xs:int">
      <xs:minInclusive value="1"/>
    </xs:restriction>
  </xs:simpleType>
    
  <xs:complexType name="RGBCaptureMeasurementType">
    <xs:sequence>
      <xs:element name="PrimaryIndex">
        <xs:complexType>
          <xs:all>
            <xs:element name="White" type="cdm:OneBasedIndex"/>
            <xs:element name="Black" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Red" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Green" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Blue" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Cyan" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Magenta" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Yellow" type="cdm:OneBasedIndex" minOccurs="0"/>
          </xs:all>
        </xs:complexType>
      </xs:element>
      <xs:element name="NeutralIndices">
        <xs:simpleType>
          <xs:list itemType="cdm:OneBasedIndex"/>
        </xs:simpleType>
      </xs:element>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:complexType name="CMYKPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeCMYKSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="GammaType">
    <xs:attribute name="value" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="GammaOffsetGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="GammaOffsetGainLinearGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="LinearGain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="cdm:FloatList"/>
      <xs:element name="Output" type="cdm:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="cdm:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="0" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="GamutBoundarySamplesType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:RGBType" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="RGBVirtualMeasurementType">
    <xs:sequence>
      <xs:element name="MaxColorantUsed" type="xs:float"/>
      <xs:element name="MinColorantUsed" type="xs:float"/>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:choice>
        <xs:element name="Gamma" type="cdm:GammaType"/>
        <xs:element name="GammaOffsetGain" type="cdm:GammaOffsetGainType"/>
        <xs:element name="GammaOffsetGainLinearGain" type="cdm:GammaOffsetGainLinearGainType"/>
        <xs:element name="HDRToneResponseCurves" type="cdm:HDRToneResponseCurvesType"/>
      </xs:choice>
      <xs:element name="GamutBoundarySamples" type="cdm:GamutBoundarySamplesType" minOccurs="0"/>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="MeasurementConditions" type="cdm:MeasurementConditionsType" minOccurs="0"/>
        <xs:element name="SelfLuminous" type="xs:boolean" />
        <xs:element name="MaxColorant" type="xs:float"/>
        <xs:element name="MinColorant" type="xs:float"/>
        <xs:choice>
          <xs:element name="CRTDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="LCDDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBProjectorDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBProjectorMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="ScannerDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CameraDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CMYKPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:CMYKPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBVirtualDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBVirtualMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
        </xs:choice>
        <xs:element name="PlugInDevice" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>

```



## <a name="wcs-cdmp-v20-calibration-addition"></a><span data-ttu-id="3d502-182">Adición de calibración de CDMP v 2.0 de WCS</span><span class="sxs-lookup"><span data-stu-id="3d502-182">WCS CDMP v2.0 Calibration Addition</span></span>

<span data-ttu-id="3d502-183">El elemento **ColorDeviceModel** del esquema CDMP se ha actualizado en Windows 7 para incluir el nuevo elemento de calibración.</span><span class="sxs-lookup"><span data-stu-id="3d502-183">The **ColorDeviceModel** element of the CDMP schema has been updated in Windows 7 to include the new calibration element.</span></span> <span data-ttu-id="3d502-184">A continuación se muestra el cambio en el esquema CDMP.</span><span class="sxs-lookup"><span data-stu-id="3d502-184">The following shows the change to the CDMP schema.</span></span>


```C++
  ...
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        ...
        <xs:element name="PlugInDevice" minOccurs="0">
             ...
        </xs:element>
        <xs:element name="Calibration" type="cal:Calibration" minOccurs="0"/>
        ...
      <xs:sequence>
    ...
    <xs:complexType>
  ...
```



## <a name="the-cdmp-schema-elements"></a><span data-ttu-id="3d502-185">Los elementos de esquema CDMP</span><span class="sxs-lookup"><span data-stu-id="3d502-185">The CDMP Schema Elements</span></span>

> [!Note]  
> <span data-ttu-id="3d502-186">Los primarios son muestras principales de rojo, verde, azul, negro y blanco.</span><span class="sxs-lookup"><span data-stu-id="3d502-186">Primaries are primary samples of red, green, blue, black, and white.</span></span> <span data-ttu-id="3d502-187">Una rampa principal es una rampa tonal de menos luminancia hasta el valor principal completo.</span><span class="sxs-lookup"><span data-stu-id="3d502-187">A primary ramp is a tonal ramp from least luminance to full primary value.</span></span> <span data-ttu-id="3d502-188">El número máximo de entradas en una rampa de tono es 4096.</span><span class="sxs-lookup"><span data-stu-id="3d502-188">The maximum number of entries in a tone ramp is 4096.</span></span>

 

> [!Note]  
> <span data-ttu-id="3d502-189">DMPs son necesarios para tener datos de medición.</span><span class="sxs-lookup"><span data-stu-id="3d502-189">DMPs are required to have measurement data.</span></span>

 

### <a name="colordevicemodelprofile"></a><span data-ttu-id="3d502-190">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="3d502-190">ColorDeviceModelProfile</span></span>

<span data-ttu-id="3d502-191">Este elemento es de tipo ColorDeviceModel.</span><span class="sxs-lookup"><span data-stu-id="3d502-191">This element is of type ColorDeviceModel.</span></span>

<span data-ttu-id="3d502-192">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-192">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="colordevicemodel"></a><span data-ttu-id="3d502-193">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="3d502-193">ColorDeviceModel</span></span>

<span data-ttu-id="3d502-194">Este elemento es una secuencia de los siguientes subelementos</span><span class="sxs-lookup"><span data-stu-id="3d502-194">This element is a sequence of the following sub-elements</span></span>

1.  <span data-ttu-id="3d502-195">Cadena de perfilename,</span><span class="sxs-lookup"><span data-stu-id="3d502-195">ProfileName string,</span></span>
2.  <span data-ttu-id="3d502-196">cadena de descripción opcional,</span><span class="sxs-lookup"><span data-stu-id="3d502-196">optional Description string,</span></span>
3.  <span data-ttu-id="3d502-197">cadena de autor opcional,</span><span class="sxs-lookup"><span data-stu-id="3d502-197">optional Author string,</span></span>
4.  <span data-ttu-id="3d502-198">opcional MeasurementConditions MeasurementConditionsType,</span><span class="sxs-lookup"><span data-stu-id="3d502-198">optional MeasurementConditions MeasurementConditionsType,</span></span>
5.  <span data-ttu-id="3d502-199">Self-Luminous Boolean,</span><span class="sxs-lookup"><span data-stu-id="3d502-199">Self-Luminous Boolean,</span></span>
6.  <span data-ttu-id="3d502-200">MaxColorant Float,</span><span class="sxs-lookup"><span data-stu-id="3d502-200">MaxColorant float,</span></span>
7.  <span data-ttu-id="3d502-201">MinColorant Float,</span><span class="sxs-lookup"><span data-stu-id="3d502-201">MinColorant float,</span></span>
8.  <span data-ttu-id="3d502-202">Elección de los elementos</span><span class="sxs-lookup"><span data-stu-id="3d502-202">Choice of elements</span></span>
    1.  <span data-ttu-id="3d502-203">CRTDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-203">CRTDevice,</span></span>
    2.  <span data-ttu-id="3d502-204">LCDDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-204">LCDDevice,</span></span>
    3.  <span data-ttu-id="3d502-205">RGBProjectorDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-205">RGBProjectorDevice,</span></span>
    4.  <span data-ttu-id="3d502-206">ScannerDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-206">ScannerDevice,</span></span>
    5.  <span data-ttu-id="3d502-207">CameraDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-207">CameraDevice,</span></span>
    6.  <span data-ttu-id="3d502-208">RGBPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-208">RGBPrinterDevice,</span></span>
    7.  <span data-ttu-id="3d502-209">CMYKPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-209">CMYKPrinterDevice,</span></span>
    8.  <span data-ttu-id="3d502-210">RGBVirtualDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-210">RGBVirtualDevice,</span></span>
9.  <span data-ttu-id="3d502-211">PlugInDevice,</span><span class="sxs-lookup"><span data-stu-id="3d502-211">PlugInDevice,</span></span>
10. <span data-ttu-id="3d502-212">Extensión opcional ExtensionType</span><span class="sxs-lookup"><span data-stu-id="3d502-212">optional Extension ExtensionType</span></span>

<span data-ttu-id="3d502-213">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-213">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="3d502-214">Los subelementos de cadena tienen un máximo de 10.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3d502-214">String sub-elements have a maximum of 10,000 characters.</span></span> <span data-ttu-id="3d502-215">El subelemento MaxColorant debe ser mayor o igual que cero (0) y mayor que el subelemento MinColorant.</span><span class="sxs-lookup"><span data-stu-id="3d502-215">The MaxColorant sub-element must be greater than or equal to zero (0) and greater than the MinColorant sub-element.</span></span> <span data-ttu-id="3d502-216">El valor de MinColorant puede ser negativo.</span><span class="sxs-lookup"><span data-stu-id="3d502-216">The MinColorant can be negative.</span></span>

### <a name="namespaceversion"></a><span data-ttu-id="3d502-217">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="3d502-217">NamespaceVersion</span></span>

<span data-ttu-id="3d502-218">xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="3d502-218">xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

<span data-ttu-id="3d502-219">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="3d502-219">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

### <a name="version"></a><span data-ttu-id="3d502-220">Versión</span><span class="sxs-lookup"><span data-stu-id="3d502-220">Version</span></span>

<span data-ttu-id="3d502-221">Versión = "1,0" con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3d502-221">Version = "1.0" with Windows Vista.</span></span>

<span data-ttu-id="3d502-222">**Condiciones de validación:** Cualquier valor de versión &gt; 0,1 o &lt; = 2,0 es válido para admitir cambios no importantes en el formato.</span><span class="sxs-lookup"><span data-stu-id="3d502-222">**Validation conditions:** Any version value &gt;0.1 or &lt;=2.0 is valid to support non-breaking changes to the format.</span></span>

### <a name="documentation"></a><span data-ttu-id="3d502-223">Documentación</span><span class="sxs-lookup"><span data-stu-id="3d502-223">Documentation</span></span>

<span data-ttu-id="3d502-224">Esquema de Perfil de modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d502-224">Device Model Profile schema.</span></span>

<span data-ttu-id="3d502-225">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d502-225">Copyright (C) Microsoft.</span></span> <span data-ttu-id="3d502-226">Todos los derechos reservados.</span><span class="sxs-lookup"><span data-stu-id="3d502-226">All rights reserved.</span></span>

### <a name="crtdevice-element"></a><span data-ttu-id="3d502-227">Elemento CRTDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-227">CRTDevice element</span></span>

<span data-ttu-id="3d502-228">Este elemento es una secuencia de subelementos de un MeasurementData DisplayMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="3d502-228">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="3d502-229">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-229">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="lcddevice-element"></a><span data-ttu-id="3d502-230">Elemento LCDDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-230">LCDDevice element</span></span>

<span data-ttu-id="3d502-231">Este elemento es una secuencia de subelementos de un MeasurementData DisplayMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="3d502-231">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="3d502-232">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-232">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="projectordevice-element"></a><span data-ttu-id="3d502-233">Elemento ProjectorDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-233">ProjectorDevice element</span></span>

<span data-ttu-id="3d502-234">Este elemento es una secuencia de subelementos de un MeasurementData RGBProjectorMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="3d502-234">This element is a sequence of sub-elements of a MeasurementData RGBProjectorMeasurementType.</span></span>

<span data-ttu-id="3d502-235">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-235">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="scannerdevice-element"></a><span data-ttu-id="3d502-236">Elemento ScannerDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-236">ScannerDevice element</span></span>

<span data-ttu-id="3d502-237">Este elemento es una secuencia de subelementos de un MeasurementData RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-237">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="3d502-238">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-238">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cameradevice-element"></a><span data-ttu-id="3d502-239">Elemento CameraDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-239">CameraDevice element</span></span>

<span data-ttu-id="3d502-240">Este elemento es una secuencia de subelementos de un MeasurementData RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-240">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="3d502-241">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-241">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbprinterdevice-element"></a><span data-ttu-id="3d502-242">Elemento RGBPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-242">RGBPrinterDevice element</span></span>

<span data-ttu-id="3d502-243">Este elemento es una secuencia de subelementos de un MeasurementData RGBPrinterMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="3d502-243">This element is a sequence of sub-elements of a MeasurementData RGBPrinterMeasurementType.</span></span>

<span data-ttu-id="3d502-244">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-244">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cmykprinterdevice-element"></a><span data-ttu-id="3d502-245">Elemento CMYKPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-245">CMYKPrinterDevice element</span></span>

<span data-ttu-id="3d502-246">Este elemento es una secuencia de subelementos de un MeasurementData CMYKPrinterMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="3d502-246">This element is a sequence of sub-elements of a MeasurementData CMYKPrinterMeasurementType.</span></span>

<span data-ttu-id="3d502-247">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-247">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbvirtualdevice-element"></a><span data-ttu-id="3d502-248">Elemento RGBVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="3d502-248">RGBVirtualDevice element</span></span>

<span data-ttu-id="3d502-249">Este elemento es una secuencia de subelementos de un RGBVirtualMeasurementDataType.</span><span class="sxs-lookup"><span data-stu-id="3d502-249">This element is a sequence of sub-elements of a RGBVirtualMeasurementDataType.</span></span>

<span data-ttu-id="3d502-250">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="3d502-250">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="plugindevicetype"></a><span data-ttu-id="3d502-251">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="3d502-251">PlugInDeviceType</span></span>

<span data-ttu-id="3d502-252">Este elemento es una secuencia de un GUIDType de GUID y cualquier subelemento.</span><span class="sxs-lookup"><span data-stu-id="3d502-252">This element is a sequence of a GUID GUIDType and any sub-elements.</span></span>

<span data-ttu-id="3d502-253">**Condiciones de validación:** El GUID se usa para hacer coincidir el GUID del archivo DLL del complemento DM.</span><span class="sxs-lookup"><span data-stu-id="3d502-253">**Validation conditions:** The GUID is used to match the DM PlugIn Dll GUID.</span></span> <span data-ttu-id="3d502-254">Hay un máximo de 100.000 subelementos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3d502-254">There are a maximum of 100,000 custom sub-elements.</span></span>

### <a name="rgbvirtualmeasurementtype"></a><span data-ttu-id="3d502-255">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-255">RGBVirtualMeasurementType</span></span>

<span data-ttu-id="3d502-256">Este elemento es una secuencia que consta de</span><span class="sxs-lookup"><span data-stu-id="3d502-256">This element is a sequence consisting of</span></span>

1.  <span data-ttu-id="3d502-257">Grupo RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="3d502-257">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="3d502-258">Una opción de</span><span class="sxs-lookup"><span data-stu-id="3d502-258">A choice of</span></span>
3.  -   <span data-ttu-id="3d502-259">Gamma</span><span class="sxs-lookup"><span data-stu-id="3d502-259">Gamma</span></span>
    -   <span data-ttu-id="3d502-260">GammaOffsetGain</span><span class="sxs-lookup"><span data-stu-id="3d502-260">GammaOffsetGain</span></span>
    -   <span data-ttu-id="3d502-261">GammaOffsetGainLinearGam</span><span class="sxs-lookup"><span data-stu-id="3d502-261">GammaOffsetGainLinearGam</span></span>
    -   <span data-ttu-id="3d502-262">Elementos ToneResponseCurves</span><span class="sxs-lookup"><span data-stu-id="3d502-262">ToneResponseCurves elements</span></span>

4.  <span data-ttu-id="3d502-263">GamutBoundarySamples GamutBoundarySamplesType opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-263">optional GamutBoundarySamples GamutBoundarySamplesType</span></span>
5.  <span data-ttu-id="3d502-264">TimeStamp dateTime</span><span class="sxs-lookup"><span data-stu-id="3d502-264">TimeStamp dateTime</span></span>

<span data-ttu-id="3d502-265">**Condiciones de validación:** Cada subelemento de estos tipos tiene sus propias condiciones de validación.</span><span class="sxs-lookup"><span data-stu-id="3d502-265">**Validation conditions:** Each sub-element of these types has its own validation conditions.</span></span>

### <a name="gammatype"></a><span data-ttu-id="3d502-266">GammaType</span><span class="sxs-lookup"><span data-stu-id="3d502-266">GammaType</span></span>

<span data-ttu-id="3d502-267">Este elemento es un tipo complejo que se compone del atributo</span><span class="sxs-lookup"><span data-stu-id="3d502-267">This element is a complex type consisting of the attribute</span></span>

-   <span data-ttu-id="3d502-268">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="3d502-268">Gamma NonNegativeFloatType</span></span>

<span data-ttu-id="3d502-269">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-269">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgaintype"></a><span data-ttu-id="3d502-270">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="3d502-270">GammaOffsetGainType</span></span>

<span data-ttu-id="3d502-271">Este elemento es un tipo complejo que consta de los atributos</span><span class="sxs-lookup"><span data-stu-id="3d502-271">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="3d502-272">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="3d502-272">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="3d502-273">Desplazamiento NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="3d502-273">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="3d502-274">Obtener NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="3d502-274">Gain NonNegativeFloatType</span></span>

<span data-ttu-id="3d502-275">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-275">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgainlineargaintype"></a><span data-ttu-id="3d502-276">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="3d502-276">GammaOffsetGainLinearGainType</span></span>

<span data-ttu-id="3d502-277">Este elemento es un tipo complejo que consta de los atributos</span><span class="sxs-lookup"><span data-stu-id="3d502-277">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="3d502-278">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="3d502-278">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="3d502-279">Desplazamiento NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="3d502-279">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="3d502-280">Obtener NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="3d502-280">Gain NonNegativeFloatType</span></span>
-   <span data-ttu-id="3d502-281">LinearGain NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="3d502-281">LinearGain NonNegativeFloatType</span></span>
-   <span data-ttu-id="3d502-282">TransitionPoint NonNegativeFloatType.</span><span class="sxs-lookup"><span data-stu-id="3d502-282">TransitionPoint NonNegativeFloatType.</span></span>

<span data-ttu-id="3d502-283">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-283">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="toneresponsecurvestype"></a><span data-ttu-id="3d502-284">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="3d502-284">ToneResponseCurvesType</span></span>

<span data-ttu-id="3d502-285">Este elemento es una secuencia de</span><span class="sxs-lookup"><span data-stu-id="3d502-285">This element is a sequence of</span></span>

1.  <span data-ttu-id="3d502-286">RedTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="3d502-286">RedTRC FloatPairList</span></span>
2.  <span data-ttu-id="3d502-287">GreenTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="3d502-287">GreenTRC FloatPairList</span></span>
3.  <span data-ttu-id="3d502-288">BlueTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="3d502-288">BlueTRC FloatPairList</span></span>

<span data-ttu-id="3d502-289">El elemento también tiene un atributo TRCLength de tipo unsignedint.</span><span class="sxs-lookup"><span data-stu-id="3d502-289">The element also has an attribute TRCLength of unsignedint type.</span></span>

<span data-ttu-id="3d502-290">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-290">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gamutboundarysamplestype"></a><span data-ttu-id="3d502-291">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="3d502-291">GamutBoundarySamplesType</span></span>

<span data-ttu-id="3d502-292">Este elemento es una secuencia de RGBTypes RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-292">This element is a sequence of RGB RGBTypes.</span></span>

<span data-ttu-id="3d502-293">**Condiciones de validación:** Repeticiones máximas sin enlazar actualmente, que se van a restringir en función de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-293">**Validation conditions:** Currently unbounded maximum occurences, to be capped based on industry feedback.</span></span>

### <a name="floatpairlist"></a><span data-ttu-id="3d502-294">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="3d502-294">FloatPairList</span></span>

<span data-ttu-id="3d502-295">Este elemento es un tipo simple de lista de pares de elementos flotantes.</span><span class="sxs-lookup"><span data-stu-id="3d502-295">This element is a simple type of list of pairs of floats.</span></span>

<span data-ttu-id="3d502-296">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-296">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="cmykprintermeasurementtype"></a><span data-ttu-id="3d502-297">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-297">CMYKPrinterMeasurementType</span></span>

<span data-ttu-id="3d502-298">Este elemento es un</span><span class="sxs-lookup"><span data-stu-id="3d502-298">This element is a</span></span>

1. <span data-ttu-id="3d502-299">secuencia del elemento ColorCube que consta de una secuencia de NonNegativeCMYKSampleType de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d502-299">sequence of ColorCube element consisting of a sequence of Sample NonNegativeCMYKSampleType</span></span>

2. <span data-ttu-id="3d502-300">Atributo TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="3d502-300">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="3d502-301">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-301">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprintermeasurementtype"></a><span data-ttu-id="3d502-302">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-302">RGBPrinterMeasurementType</span></span>

<span data-ttu-id="3d502-303">Este elemento es un</span><span class="sxs-lookup"><span data-stu-id="3d502-303">This element is a</span></span>

1. <span data-ttu-id="3d502-304">secuencia del elemento ColorCube que consta de una secuencia de NonNegativeRGBSampleType de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d502-304">sequence of ColorCube element consisting of a sequence of Sample NonNegativeRGBSampleType</span></span>

2. <span data-ttu-id="3d502-305">Atributo TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="3d502-305">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="3d502-306">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-306">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbcapturemeasurementtype"></a><span data-ttu-id="3d502-307">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-307">RGBCaptureMeasurementType</span></span>

<span data-ttu-id="3d502-308">Este elemento es una secuencia de</span><span class="sxs-lookup"><span data-stu-id="3d502-308">This element is a sequence of</span></span>

1.  <span data-ttu-id="3d502-309">PrimaryIndex complexType de</span><span class="sxs-lookup"><span data-stu-id="3d502-309">PrimaryIndex complexType of</span></span>
2.  1.  <span data-ttu-id="3d502-310">OneBasedIndex blanco</span><span class="sxs-lookup"><span data-stu-id="3d502-310">White OneBasedIndex</span></span>
    2.  <span data-ttu-id="3d502-311">OneBasedIndex negro opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-311">Optional Black OneBasedIndex</span></span>
    3.  <span data-ttu-id="3d502-312">OneBasedIndex rojo opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-312">Optional Red OneBasedIndex</span></span>
    4.  <span data-ttu-id="3d502-313">OneBasedIndex verde opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-313">Optional Green OneBasedIndex</span></span>
    5.  <span data-ttu-id="3d502-314">OneBasedIndex azul opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-314">Optional Blue OneBasedIndex</span></span>
    6.  <span data-ttu-id="3d502-315">OneBasedIndex cian opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-315">Optional Cyan OneBasedIndex</span></span>
    7.  <span data-ttu-id="3d502-316">OneBasedIndex magenta opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-316">Optional Magenta OneBasedIndex</span></span>
    8.  <span data-ttu-id="3d502-317">OneBasedIndex amarillo opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-317">Optional Yellow OneBasedIndex</span></span>

3.  <span data-ttu-id="3d502-318">NeutralIndices de líneas de OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="3d502-318">NeutralIndices of lines of OneBasedIndex</span></span>
4.  <span data-ttu-id="3d502-319">ColorSamples secuencia de NonNegativeRGBSampleType de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d502-319">ColorSamples sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="3d502-320">El elemento también tiene un atributo TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="3d502-320">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="3d502-321">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-321">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="onebasedindex"></a><span data-ttu-id="3d502-322">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="3d502-322">OneBasedIndex</span></span>

<span data-ttu-id="3d502-323">Este elemento es un tipo simple del int sin signo de base de restricción con valor de minInclusive = "1".</span><span class="sxs-lookup"><span data-stu-id="3d502-323">This element is a simple type of restriction base unsigned int with minInclusive value = "1."</span></span>

<span data-ttu-id="3d502-324">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-324">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprojectormeasurementtype"></a><span data-ttu-id="3d502-325">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-325">RGBProjectorMeasurementType</span></span>

<span data-ttu-id="3d502-326">Este elemento es una secuencia de</span><span class="sxs-lookup"><span data-stu-id="3d502-326">This element is a sequence of</span></span>

1.  <span data-ttu-id="3d502-327">Grupo RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="3d502-327">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="3d502-328">elemento ColorSamples que consta de una secuencia de NonNegativeRGBSampleType de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d502-328">element ColorSamples consisting of sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="3d502-329">El elemento también tiene un atributo TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="3d502-329">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="3d502-330">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-330">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="displaymeasurementtype"></a><span data-ttu-id="3d502-331">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="3d502-331">DisplayMeasurementType</span></span>

<span data-ttu-id="3d502-332">Este elemento es una secuencia de</span><span class="sxs-lookup"><span data-stu-id="3d502-332">This element is a sequence of</span></span>

1.  <span data-ttu-id="3d502-333">Grupo RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="3d502-333">group RGBPrimariesGroup</span></span>
2.  <span data-ttu-id="3d502-334">GrayRamp de la secuencia de NonNegativeRGBType de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d502-334">GrayRamp of sequence of Sample NonNegativeRGBType</span></span>
3.  <span data-ttu-id="3d502-335">RedRamp de la secuencia de NonNegativeRGBType de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d502-335">RedRamp of sequence of Sample NonNegativeRGBType</span></span>
4.  <span data-ttu-id="3d502-336">GreenRamp de la secuencia de NonNegativeRGBType de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d502-336">GreenRamp of sequence of Sample NonNegativeRGBType</span></span>
5.  <span data-ttu-id="3d502-337">BlueRamp de la secuencia de NonNegativeRGBType de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d502-337">BlueRamp of sequence of Sample NonNegativeRGBType</span></span>

<span data-ttu-id="3d502-338">El elemento DisplayMeasurementType también tiene un atributo TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="3d502-338">The DisplayMeasurementType element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="3d502-339">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-339">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="measurementconditionstype"></a><span data-ttu-id="3d502-340">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="3d502-340">MeasurementConditionsType</span></span>

<span data-ttu-id="3d502-341">MeasurementConditionsType es una secuencia de subelementos que contiene:</span><span class="sxs-lookup"><span data-stu-id="3d502-341">The MeasurementConditionsType is a sequence of sub-elements that contains:</span></span>

1.  <span data-ttu-id="3d502-342">ColorSpace valor de enumeración de cadena restringida de "CIEXYZ"</span><span class="sxs-lookup"><span data-stu-id="3d502-342">ColorSpace restricted string enumeration value of "CIEXYZ"</span></span>
2.  <span data-ttu-id="3d502-343">Elección opcional de WhitePoint NonNegativeXYZType o WhitePointName enumeración de la cadena de los valores D50, D65, A o F2</span><span class="sxs-lookup"><span data-stu-id="3d502-343">optional choice of WhitePoint NonNegativeXYZType or WhitePointName string enumeration of values D50, D65, A, or F2</span></span>
3.  <span data-ttu-id="3d502-344">Geometría GeometryType</span><span class="sxs-lookup"><span data-stu-id="3d502-344">Geometry GeometryType</span></span>
4.  <span data-ttu-id="3d502-345">Entero de ApertureSize en milímetros</span><span class="sxs-lookup"><span data-stu-id="3d502-345">ApertureSize integer in millimeters</span></span>

<span data-ttu-id="3d502-346">Los valores predeterminados son:</span><span class="sxs-lookup"><span data-stu-id="3d502-346">Defaults are:</span></span>

1.  <span data-ttu-id="3d502-347">Impresoras RGB y CMYK:</span><span class="sxs-lookup"><span data-stu-id="3d502-347">RGB and CMYK Printers:</span></span>
    1.  <span data-ttu-id="3d502-348">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="3d502-348">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="3d502-349">D50 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="3d502-349">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="3d502-350">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="3d502-350">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="3d502-351">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="3d502-351">10mm ApertureSize</span></span>
2.  <span data-ttu-id="3d502-352">Escáneres</span><span class="sxs-lookup"><span data-stu-id="3d502-352">Scanners:</span></span>
    1.  <span data-ttu-id="3d502-353">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="3d502-353">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="3d502-354">D50 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="3d502-354">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="3d502-355">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="3d502-355">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="3d502-356">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="3d502-356">10mm ApertureSize</span></span>
3.  <span data-ttu-id="3d502-357">Muestra el dispositivo virtual RGB:</span><span class="sxs-lookup"><span data-stu-id="3d502-357">Displays and RGB Virtual Device:</span></span>
    1.  <span data-ttu-id="3d502-358">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="3d502-358">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="3d502-359">WhitePointValue D65</span><span class="sxs-lookup"><span data-stu-id="3d502-359">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="3d502-360">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="3d502-360">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="3d502-361">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="3d502-361">10mm ApertureSize</span></span>
4.  <span data-ttu-id="3d502-362">Cámaras</span><span class="sxs-lookup"><span data-stu-id="3d502-362">Cameras:</span></span>
    1.  <span data-ttu-id="3d502-363">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="3d502-363">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="3d502-364">WhitePointValue D65</span><span class="sxs-lookup"><span data-stu-id="3d502-364">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="3d502-365">GeometryType directo</span><span class="sxs-lookup"><span data-stu-id="3d502-365">Direct GeometryType</span></span>
    4.  <span data-ttu-id="3d502-366">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="3d502-366">10mm ApertureSize</span></span>

<span data-ttu-id="3d502-367">**Condiciones de validación:** La validación de cada subelemento se determina mediante condiciones de validación para esos subelementos.</span><span class="sxs-lookup"><span data-stu-id="3d502-367">**Validation conditions:** Validation of each sub-element is determined by validation conditions for those sub-elements.</span></span> <span data-ttu-id="3d502-368">Si falta un subelemento, se usa el tipo de modelo de dispositivo predeterminado específico.</span><span class="sxs-lookup"><span data-stu-id="3d502-368">If any sub-element is missing, the device model type specific default is used.</span></span>

### <a name="geometrytype"></a><span data-ttu-id="3d502-369">GeometryType</span><span class="sxs-lookup"><span data-stu-id="3d502-369">GeometryType</span></span>

<span data-ttu-id="3d502-370">String</span><span class="sxs-lookup"><span data-stu-id="3d502-370">String</span></span>

<span data-ttu-id="3d502-371">Valores de enumeración:</span><span class="sxs-lookup"><span data-stu-id="3d502-371">Enumeration values:</span></span>

-   <span data-ttu-id="3d502-372">"0/45"</span><span class="sxs-lookup"><span data-stu-id="3d502-372">"0/45"</span></span>
-   <span data-ttu-id="3d502-373">"0/difuso"</span><span class="sxs-lookup"><span data-stu-id="3d502-373">"0/diffuse"</span></span>
-   <span data-ttu-id="3d502-374">"difuso/0"</span><span class="sxs-lookup"><span data-stu-id="3d502-374">"diffuse/0"</span></span>
-   <span data-ttu-id="3d502-375">Directo</span><span class="sxs-lookup"><span data-stu-id="3d502-375">"Direct"</span></span>

<span data-ttu-id="3d502-376">**Condiciones de validación:** Cualquier valor, excepto los valores de enumberation enumerados, no es válido.</span><span class="sxs-lookup"><span data-stu-id="3d502-376">**Validation conditions:** Any value except the enumberation values listed is invalid.</span></span> <span data-ttu-id="3d502-377">Esta información no cambiará el comportamiento de procesamiento de línea base.</span><span class="sxs-lookup"><span data-stu-id="3d502-377">This information will not change baseline processing behavior.</span></span>

### <a name="rgbprimariesgroup"></a><span data-ttu-id="3d502-378">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="3d502-378">RGBPrimariesGroup</span></span>

<span data-ttu-id="3d502-379">Este elemento es una secuencia de</span><span class="sxs-lookup"><span data-stu-id="3d502-379">This element is a sequence of</span></span>

1.  <span data-ttu-id="3d502-380">WhitePrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-380">WhitePrimary NonNegativeXYZType</span></span>
2.  <span data-ttu-id="3d502-381">RedPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-381">RedPrimary NonNegativeXYZType</span></span>
3.  <span data-ttu-id="3d502-382">GreenPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-382">GreenPrimary NonNegativeXYZType</span></span>
4.  <span data-ttu-id="3d502-383">BluePrimary NonNegativeXYZTYpe</span><span class="sxs-lookup"><span data-stu-id="3d502-383">BluePrimary NonNegativeXYZTYpe</span></span>
5.  <span data-ttu-id="3d502-384">BlackPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-384">BlackPrimary NonNegativeXYZType</span></span>

<span data-ttu-id="3d502-385">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-385">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyksampletype"></a><span data-ttu-id="3d502-386">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="3d502-386">NonNegativeCMYKSampleType</span></span>

<span data-ttu-id="3d502-387">Este elemento es una secuencia de</span><span class="sxs-lookup"><span data-stu-id="3d502-387">This element is a sequence of</span></span>

1.  <span data-ttu-id="3d502-388">CMYK NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="3d502-388">CMYK NonNegativeCMYKType</span></span>
2.  <span data-ttu-id="3d502-389">CIEXYZ NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-389">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="3d502-390">El elemento también tiene una cadena de etiqueta de atributo opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-390">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="3d502-391">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-391">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbsampletype"></a><span data-ttu-id="3d502-392">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="3d502-392">NonNegativeRGBSampleType</span></span>

<span data-ttu-id="3d502-393">Este elemento es una secuencia de</span><span class="sxs-lookup"><span data-stu-id="3d502-393">This element is a sequence of</span></span>

1.  <span data-ttu-id="3d502-394">RGB NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="3d502-394">RGB NonNegativeRGBType</span></span>
2.  <span data-ttu-id="3d502-395">CIEXYZ NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-395">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="3d502-396">El elemento también tiene una cadena de etiqueta de atributo opcional</span><span class="sxs-lookup"><span data-stu-id="3d502-396">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="3d502-397">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-397">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyktype"></a><span data-ttu-id="3d502-398">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="3d502-398">NonNegativeCMYKType</span></span>

<span data-ttu-id="3d502-399">Este elemento se compone de atributos</span><span class="sxs-lookup"><span data-stu-id="3d502-399">This element consisting of attributes</span></span>

1.  <span data-ttu-id="3d502-400">C Float</span><span class="sxs-lookup"><span data-stu-id="3d502-400">C float</span></span>
2.  <span data-ttu-id="3d502-401">M Float</span><span class="sxs-lookup"><span data-stu-id="3d502-401">M float</span></span>
3.  <span data-ttu-id="3d502-402">Float Y</span><span class="sxs-lookup"><span data-stu-id="3d502-402">Y float</span></span>
4.  <span data-ttu-id="3d502-403">K Float</span><span class="sxs-lookup"><span data-stu-id="3d502-403">K float</span></span>

<span data-ttu-id="3d502-404">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-404">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbtype"></a><span data-ttu-id="3d502-405">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="3d502-405">NonNegativeRGBType</span></span>

<span data-ttu-id="3d502-406">Este elemento se compone de atributos</span><span class="sxs-lookup"><span data-stu-id="3d502-406">This element consisting of attributes</span></span>

1.  <span data-ttu-id="3d502-407">R Float</span><span class="sxs-lookup"><span data-stu-id="3d502-407">R float</span></span>
2.  <span data-ttu-id="3d502-408">G Float</span><span class="sxs-lookup"><span data-stu-id="3d502-408">G float</span></span>
3.  <span data-ttu-id="3d502-409">B Float</span><span class="sxs-lookup"><span data-stu-id="3d502-409">B float</span></span>

<span data-ttu-id="3d502-410">**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.</span><span class="sxs-lookup"><span data-stu-id="3d502-410">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="extensiontype"></a><span data-ttu-id="3d502-411">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="3d502-411">ExtensionType</span></span>

<span data-ttu-id="3d502-412">El elemento ExtensionType es una secuencia de cualquier tipo de subelemento y se usa para obtener información de propiedad de aplicaciones que no son de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d502-412">The ExtensionType element is a sequence of any sub-element type and is used for proprietary information from non-Microsoft applications.</span></span>

<span data-ttu-id="3d502-413">**Condiciones de validación:** Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3d502-413">**Validation conditions:** This element is optional.</span></span> <span data-ttu-id="3d502-414">Puede haber un máximo de 1000 subelementos de extensión.</span><span class="sxs-lookup"><span data-stu-id="3d502-414">There can be a maximum of 1000 extension sub-elements.</span></span>

### <a name="nonnegativexyztype"></a><span data-ttu-id="3d502-415">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-415">NonNegativeXYZType</span></span>

<span data-ttu-id="3d502-416">El elemento NonNegativeXYZType se compone de NonNegativeFloatType tres elementos de punto flotante de IEEE de precisión sencilla denominados "X", "Y" y "Z".</span><span class="sxs-lookup"><span data-stu-id="3d502-416">The NonNegativeXYZType element is composed of NonNegativeFloatType three single-precision IEEE floating-point elements named "X," "Y," and "Z."</span></span> <span data-ttu-id="3d502-417">Estos valores se limitan a los valores de medida de los perfiles DMP.</span><span class="sxs-lookup"><span data-stu-id="3d502-417">These values are limited to the DMP profiles measurement values.</span></span> <span data-ttu-id="3d502-418">Estas medidas pueden ser absolutas (no relativas) CIEXYZ 1931 valores reflectantes o valores absolutos (no relativos) CIEXYZ 1931 Direct (transpermisivo) en candelas por unidades cuadradas.</span><span class="sxs-lookup"><span data-stu-id="3d502-418">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="3d502-419">**Condiciones de validación:** Solo son válidos los valores del mundo real y los valores de medida CIEXYZ negativos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="3d502-419">**Validation conditions:** Only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="3d502-420">Dado que se trata de valores absolutos, los valores pueden ser mayores que 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="3d502-420">Because these are absolute values, values can be greater than 1.0f.</span></span> <span data-ttu-id="3d502-421">Un límite razonable para cualquier "X", "Y" o "Z".</span><span class="sxs-lookup"><span data-stu-id="3d502-421">A reasonable limit for any "X," "Y," or "Z."</span></span> <span data-ttu-id="3d502-422">el valor se establece de forma arbitraria en 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="3d502-422">value is arbitrarily set to 10000.0f.</span></span>

### <a name="xyztype"></a><span data-ttu-id="3d502-423">XYZType</span><span class="sxs-lookup"><span data-stu-id="3d502-423">XYZType</span></span>

<span data-ttu-id="3d502-424">El elemento XYZType se compone de tres valores de punto flotante de IEEE de precisión sencilla: "X", "Y" y "Z".</span><span class="sxs-lookup"><span data-stu-id="3d502-424">The XYZType element is composed of three single-precision IEEE floating-point values: "X," "Y," and "Z."</span></span>

## <a name="the-cdmp-baseline-algorithms"></a><span data-ttu-id="3d502-425">Algoritmos de línea de base de CDMP</span><span class="sxs-lookup"><span data-stu-id="3d502-425">The CDMP Baseline Algorithms</span></span>

### <a name="crt-device-model-baseline"></a><span data-ttu-id="3d502-426">Línea de base del modelo de dispositivo CRT</span><span class="sxs-lookup"><span data-stu-id="3d502-426">CRT Device Model Baseline</span></span>

<span data-ttu-id="3d502-427">Para entender este modelo, debe tener en cuenta el proceso de caracterización y el modelado de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3d502-427">To understand this model, you must consider both the characterization process and the device modeling.</span></span> <span data-ttu-id="3d502-428">En el proceso de caracterización, las mediciones XYZ se realizan primero en los colores obtenidos al llenar el búfer de pantalla de un dispositivo de pantalla CRT.</span><span class="sxs-lookup"><span data-stu-id="3d502-428">In the characterization process, XYZ measurements are first performed on the colors obtained by filling the display buffer of a CRT display device.</span></span> <span data-ttu-id="3d502-429">En los valores de ejemplo siguientes se generarán buenos datos para el modelo de dispositivo CRT de línea base:</span><span class="sxs-lookup"><span data-stu-id="3d502-429">The following example values will generate good data for the baseline CRT device model:</span></span>

<span data-ttu-id="3d502-430">Rojo: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-430">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="3d502-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="3d502-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="3d502-433">Neutros: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255</span><span class="sxs-lookup"><span data-stu-id="3d502-433">Neutrals: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255</span></span>

<span data-ttu-id="3d502-434">También se pueden usar incrementos distintos de 15 y incrementos no lineales.</span><span class="sxs-lookup"><span data-stu-id="3d502-434">Increments other than 15 and nonlinear increments can also be used.</span></span> <span data-ttu-id="3d502-435">Cada rampa roja, verde, azul y neutra debe contener al menos tres ejemplos, pero se recomienda proporcionar más ejemplos.</span><span class="sxs-lookup"><span data-stu-id="3d502-435">Each red, green, blue, and neutral ramp must contain at least three samples, but providing more samples is recommended.</span></span> <span data-ttu-id="3d502-436">Debe proporcionar ejemplos de rojo, verde, azul, negro y blanco puros.</span><span class="sxs-lookup"><span data-stu-id="3d502-436">You must provide samples for pure red, green, blue, black, and white.</span></span> <span data-ttu-id="3d502-437">No es necesario que los ejemplos estén espaciados uniformemente.</span><span class="sxs-lookup"><span data-stu-id="3d502-437">The samples do not have to be uniformly spaced.</span></span>

<span data-ttu-id="3d502-438">El proceso de creación de la matriz de triestímulos consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="3d502-438">The process of building the tristimulus matrix consists of two steps.</span></span> <span data-ttu-id="3d502-439">En primer lugar, calcule el valor XYZ del punto negro o el flar.</span><span class="sxs-lookup"><span data-stu-id="3d502-439">First, estimate the black point XYZ value, or the flare.</span></span> <span data-ttu-id="3d502-440">Este paso se basa en gran medida en el trabajo de Bernas \[ 3 \] con una función objetiva ligeramente modificada para la optimización no lineal.</span><span class="sxs-lookup"><span data-stu-id="3d502-440">This step is based largely on work of Berns\[3\] with a slightly modified objective function for the nonlinear optimization.</span></span> <span data-ttu-id="3d502-441">En segundo lugar, calcule la matriz de triestímulo basada en el resultado del paso uno y, además, desde un cálculo de promedio en todas las medidas por canal, no solo para el número máximo de recuentos digitales.</span><span class="sxs-lookup"><span data-stu-id="3d502-441">Second, calculate tristimulus matrix based on the result from step one and also from an averaging calculation on all of the per-channel measurements, not just the one for maximum digital count.</span></span>

<span data-ttu-id="3d502-442">Cada uno de estos pasos contiene procedimientos detallados.</span><span class="sxs-lookup"><span data-stu-id="3d502-442">Each of these steps contains detailed procedures.</span></span> <span data-ttu-id="3d502-443">El punto de partida es las rampas (17 pasos en nuestro ejemplo) para cada uno de los canales R, G y B.</span><span class="sxs-lookup"><span data-stu-id="3d502-443">The starting point is the ramps (17 steps in our example) for each of R, G, and B channels.</span></span> <span data-ttu-id="3d502-444">Cuando las medidas XYZ se representan en el plano *XY* de cromaticidad, se muestra una situación típica en la figura 1.</span><span class="sxs-lookup"><span data-stu-id="3d502-444">When the XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="3d502-445">El paso uno consiste en resolver un problema de optimización no lineal para encontrar el punto negro "mejor ajuste" que minimizará el desfase en la cromaticidad a medida que atraviesa los canales R, G y B.</span><span class="sxs-lookup"><span data-stu-id="3d502-445">Step one consists of solving a nonlinear optimization problem to find the "best fit" black point that will minimize the drift in chromaticity as one traverses along the R, G, and B channels.</span></span> <span data-ttu-id="3d502-446">Según \[ las Berna 3 \] , buscamos ( *X <sub>k</sub>*,*y <sub>k</sub>*,*Z <sub>k</sub>* ), lo que minimiza la siguiente función objetiva:</span><span class="sxs-lookup"><span data-stu-id="3d502-446">Based on Berns\[3\], we seek ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ) that minimizes the following objective function:</span></span>

![Muestra la función objetiva donde Sr, SG y SB son el conjunto de puntos de datos de los canales R, G y B.](images/cdmp-formula1.png)

<span data-ttu-id="3d502-448">donde *s <sub>R</sub>*,*s <sub>G</sub>* y *s <sub>B</sub>* son el conjunto de puntos de datos correspondientes a los puntos de los canales R, G y B.</span><span class="sxs-lookup"><span data-stu-id="3d502-448">where *S <sub>R</sub>*,*S <sub>G</sub>*, and *S<sub>B</sub>* are the set of data points corresponding to the points on the R, G, and B channels.</span></span> <span data-ttu-id="3d502-449">Para *cualquier conjunto, defina:*</span><span class="sxs-lookup"><span data-stu-id="3d502-449">For any set *S*, define:</span></span>

![Muestra una fórmula para definir cualquier conjunto.](images/cdmp-formula2.png)

<span data-ttu-id="3d502-451">En el ejemplo anterior, \| *s* \| es la cardinalidad de *s*, es decir, el número de puntos del conjunto *S*. ![ Muestra una fórmula para la cromaticidad de un punto.](images/cdmp-formula3.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-451">In the preceding, \| *S* \| is the cardinality of *S*, i.e., the number of points in the set *S*. ![Shows a formula for the chromaticity of a point.](images/cdmp-formula3.png)</span></span> <span data-ttu-id="3d502-452">es las coordenadas de cromaticidad del punto que ![ muestra un formaula para un punto.](images/cdmp-formula4.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-452">is the chromaticity coordinates of the point ![Shows a formaula for a point.](images/cdmp-formula4.png)</span></span> <span data-ttu-id="3d502-453">, de modo que ![ se muestra una fórmula para el promedio o el centro de la masa. ](images/cdmp-formula5.png) , es el promedio, o centro de masa, de todos los puntos del conjunto *S* del plano de cromaticidad.</span><span class="sxs-lookup"><span data-stu-id="3d502-453">, so ![Shows a formula for the average or center of mass.](images/cdmp-formula5.png), is the average, or center of mass, of all the points in the set *S* in the chromaticity plane.</span></span> <span data-ttu-id="3d502-454">Por lo tanto, ![ muestra una fórmula para la suma de un segundo momento de puntos.](images/cdmp-formula6.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-454">Thus, ![Shows a formula for the sum of a second moments of points.](images/cdmp-formula6.png)</span></span> <span data-ttu-id="3d502-455">es la suma de segundos de los puntos del centro de masa y es una medida de cómo se distribuyen los puntos.</span><span class="sxs-lookup"><span data-stu-id="3d502-455">is the sum of second moments of the points about the center of mass and is a measure of how spread out the points are about it.</span></span> <span data-ttu-id="3d502-456">Por último, ![ muestra una fórmula para la medida total de la distribución de tres clústeres de puntos.](images/cdmp-formula7.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-456">Finally, ![Shows a formula for the total measure of the spread of three clusters of points.](images/cdmp-formula7.png)</span></span> <span data-ttu-id="3d502-457">es una medida total de cómo se distribuyen los tres clústeres de puntos sobre sus respectivos centros de masa.</span><span class="sxs-lookup"><span data-stu-id="3d502-457">is a total measure of how spread out the three clusters of points are about their respective centers of mass.</span></span>

<span data-ttu-id="3d502-458">En el cálculo de se ![ muestra una fórmula de f (X, Y, Z; X KB, YK, ZK).](images/cdmp-formula8.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-458">In the calculation of ![Shows a formula of f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png)</span></span> <span data-ttu-id="3d502-459">, si ![ muestra una fórmula para X. ](images/cdmp-formula9.png) , se omite el cálculo y la cardinalidad de *S* se ajusta en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="3d502-459">, if ![Shows a formula for X.](images/cdmp-formula9.png) , then the calculation is skipped, and the cardinality of *S* is adjusted accordingly.</span></span>

<span data-ttu-id="3d502-460">A pesar de la complejidad aparente de la función de objetivo, es una suma de los cuadrados de muchas funciones de diferenciable en *X <sub>k</sub>*, y *<sub>k</sub>Z <sub>k</sub>* (17 puntos 2 *XY* -Components 3 Channels = 102, en el ejemplo) y, por lo tanto, es receptiva a las técnicas estándar de los mínimos no lineales, como el algoritmo de Levenberg-Marquardt, que es el algoritmo que se</span><span class="sxs-lookup"><span data-stu-id="3d502-460">Despite the apparent complexity of the objective function, it is a sum of the squares of many differentiable functions in *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 points   2 *xy* -components   3 channels = 102, in the example), and, therefore, is amenable to standard nonlinear least squares techniques, such as the Levenberg-Marquardt algorithm, which is the algorithm used in WCS.</span></span> <span data-ttu-id="3d502-461">Tenga en cuenta que la función de objetivo anterior es diferente de la que se sugiere en Berna \[ 3 en cuanto a \] que la última función mide la varianza de las distancias desde el centro de la masa, de modo que la varianza sea cero cuando los puntos sean equidistantes desde el centro de la masa, incluso aunque puedan repartirse bastante.</span><span class="sxs-lookup"><span data-stu-id="3d502-461">Note that the preceding objective function is different from the one suggested in Berns\[3\] in that the latter function measures the variance of the distances from the center of mass, so that the variance is zero when the points are equidistant from the center of mass, even though they may spread out quite a bit about it.</span></span> <span data-ttu-id="3d502-462">En el ejemplo, la dispersión de puntos se indica directamente mediante los segundos.</span><span class="sxs-lookup"><span data-stu-id="3d502-462">In the example, the dispersion of points is contolled directly using the second moments.</span></span>

<span data-ttu-id="3d502-463">Como con cualquier algoritmo iterativo del problema de los mínimos cuadrados no lineales, Levenberg-Marquardt requiere una estimación inicial.</span><span class="sxs-lookup"><span data-stu-id="3d502-463">As with any iterative algorithm for the nonlinear least squares problem, Levenberg-Marquardt requires an initial guess.</span></span> <span data-ttu-id="3d502-464">Hay dos candidatos obvios.</span><span class="sxs-lookup"><span data-stu-id="3d502-464">There are two obvious candidates.</span></span> <span data-ttu-id="3d502-465">Uno es (0, 0, 0); el otro es el punto negro medido.</span><span class="sxs-lookup"><span data-stu-id="3d502-465">One is (0, 0, 0); the other is the measured black point.</span></span> <span data-ttu-id="3d502-466">En el caso de la CTE, el punto negro medido se usa primero como la estimación inicial.</span><span class="sxs-lookup"><span data-stu-id="3d502-466">For the CTE, the measured black point is first used as the initial guess.</span></span> <span data-ttu-id="3d502-467">Si se supera un máximo de 100 iteraciones sin alcanzar un umbral de una distancia media de 0,001 de cada punto desde su centro de masa (que corresponde a un valor de umbral de (0,001) 17 3 = 0,000051 para la función de objetivo), se realiza otra ronda de iteraciones con la estimación inicial de (0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="3d502-467">If a maximum of 100 iterations is exceeded without achieving a threshold of an average distance of 0.001 of each point from its center of mass (which corresponds to a threshold value of (0.001)    17   3 = 0.000051 for the objective function), then another round of iterations with the initial guess of (0, 0, 0) is performed.</span></span> <span data-ttu-id="3d502-468">La estimación resultante del punto negro es XYZ en comparación con la mejor estimación del redondeo anterior de iteraciones (con el punto negro medido como la estimación inicial).</span><span class="sxs-lookup"><span data-stu-id="3d502-468">The resulting estimate of the black point is XYZ compared with the best estimate from the previous round of iterations (with the measured black point as the initial guess).</span></span> <span data-ttu-id="3d502-469">Use la estimación que proporciona el valor más pequeño para la función de objetivo.</span><span class="sxs-lookup"><span data-stu-id="3d502-469">Use the estimate that gives the smallest value for the objective function.</span></span> <span data-ttu-id="3d502-470">La elección de las iteraciones 100 y la distancia de error de 0,001 se seleccionan de forma empírica.</span><span class="sxs-lookup"><span data-stu-id="3d502-470">The choice of 100 iterations and the error distance of 0.001 were each selected empirically.</span></span> <span data-ttu-id="3d502-471">En versiones futuras, podría ser razonable parametrizar la distancia del error.</span><span class="sxs-lookup"><span data-stu-id="3d502-471">In future versions, it might be reasonable to parameterize the error distance.</span></span>

<span data-ttu-id="3d502-472">El resultado del paso uno es el punto negro Estimado ( *X <sub>k</sub>*,*y <sub>k</sub>*,*Z <sub>k</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="3d502-472">The result of step one is the estimated black point ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ).</span></span> <span data-ttu-id="3d502-473">El paso dos consiste en determinar la matriz de triestímulos calculando el promedio de la cromaticidad de los puntos en los tres clústeres obtenidos en el paso uno.</span><span class="sxs-lookup"><span data-stu-id="3d502-473">Step two consists of determining the tristimulus matrix by averaging the chromaticity of the points in the three clusters obtained in step one.</span></span> <span data-ttu-id="3d502-474">En el caso de los CRT, esto se hace principalmente para minimizar los efectos de los errores de medición.</span><span class="sxs-lookup"><span data-stu-id="3d502-474">For CRTs, this is done primarily to minimize the effects of measurement errors.</span></span> <span data-ttu-id="3d502-475">Los puntos que se usan para calcular el promedio de la cromaticidad deben ser los mismos puntos que se usan en la optimización del paso uno.</span><span class="sxs-lookup"><span data-stu-id="3d502-475">The points used in averaging the chromaticity must be the same points used in the optimization in step one.</span></span> <span data-ttu-id="3d502-476">En otras palabras, si el primer punto (el recuento digital 15, en el ejemplo) en cada rampa se descarta en el paso de optimización, se debe hacer lo mismo en el promedio.</span><span class="sxs-lookup"><span data-stu-id="3d502-476">In other words, if the first point (digital count 15, in the example) in each ramp is discarded in the optimization step, then the same must be done in the averaging.</span></span> <span data-ttu-id="3d502-477">Si ![ muestra fórmulas de cromaticidad promediada para las coordenadas de los canales rojo y verde.](images/cdmp-formula10.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-477">If ![Shows formulas of averaged chromaticity for coordinates in the red and green channels.](images/cdmp-formula10.png)</span></span> <span data-ttu-id="3d502-478">y ![ muestra una fórmula de cromaticidad promediada para las coordenadas del canal azul.](images/cdmp-formula11.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-478">, and ![Shows a formula of averaged chromaticity for coordinates in the blue channel.](images/cdmp-formula11.png)</span></span> <span data-ttu-id="3d502-479">son las coordenadas de cromaticidad promedio de los canales rojo, verde y azul; a continuación, el siguiente procedimiento determina la matriz de Triestímulo.</span><span class="sxs-lookup"><span data-stu-id="3d502-479">are the averaged chromaticity coordinates of the red, green, and blue channels, then the following procedure determines the tristimulus matrix.</span></span> <span data-ttu-id="3d502-480">En primer lugar, solucione el sistema lineal 3? 3:</span><span class="sxs-lookup"><span data-stu-id="3d502-480">First, solve the 3?3 linear system:</span></span>

![Muestra la primera parte del procedimiento para resolver un sistema lineal de 3? 3.](images/cdmp-formula12.png)

![Muestra la segunda parte del sistema lineal 3? 3.](images/cdmp-formula13.gif)![Muestra el valor b del subscript t al final de la segunda parte del sistema lineal 3? 3.](images/cdmp-formula14.gif)

<span data-ttu-id="3d502-484">*X <sub>w</sub>*,*y <sub>w</sub>*,*Z <sub>w</sub>*</span><span class="sxs-lookup"><span data-stu-id="3d502-484">*X <sub>W</sub>*,*Y <sub>W</sub>*,*Z<sub>W</sub>*</span></span>

![Muestra la parte final del procedimiento para resolver un sistema lineal de 3? 3.](images/cdmp-formula15.png)

<span data-ttu-id="3d502-486">Una vez determinada la matriz de triestímulo, la determinación de las curvas de tono sigue el enfoque estándar.</span><span class="sxs-lookup"><span data-stu-id="3d502-486">After the tristimulus matrix is determined, the determination of tone curves follows the standard approach.</span></span> <span data-ttu-id="3d502-487">En el caso de las pantallas de CRT, se supone que los canales individuales siguen el modelo "GOG":</span><span class="sxs-lookup"><span data-stu-id="3d502-487">For CRT displays, the individual channels are assumed to follow the "GOG" model:</span></span>

![Muestra la fórmula del modelo ' G O G '.](images/cdmp-formula16.png)

<span data-ttu-id="3d502-489">donde *k <sub>g</sub>* es la "ganancia", 1-*k <sub>g</sub>* es el "desplazamiento" y?</span><span class="sxs-lookup"><span data-stu-id="3d502-489">where *k <sub>g</sub>* is the "gain",1 -*k<sub>g</sub>* is the "offset", and ?</span></span> <span data-ttu-id="3d502-490">es el "gamma".</span><span class="sxs-lookup"><span data-stu-id="3d502-490">is the "gamma."</span></span> <span data-ttu-id="3d502-491">La matriz inversa de la matriz de triestímulo se aplica a los datos XYZ de los neutros para obtener los datos RGB lineales, que después se correlacionan con los valores RGB digitales mediante la regresión no lineal en el modelo GOG.</span><span class="sxs-lookup"><span data-stu-id="3d502-491">The inverse matrix of the tristimulus matrix is applied to the XYZ data of the neutrals to obtain the linear RGB data, which is then correlated with the digital RGB values using nonlinear regression on the GOG model.</span></span> <span data-ttu-id="3d502-492">Estas características no tienen que ser las mismas para los canales R, G y B y, por lo general, no son iguales.</span><span class="sxs-lookup"><span data-stu-id="3d502-492">These characteristics do not have to be the same for the R, G, and B channels, and generally are not the same.</span></span>

<span data-ttu-id="3d502-493">Berna \[ 1 \] : los *principios de Billmeyer y Saltzman de la tecnología de color*, 3 <sub>Rd</sub> Ed.</span><span class="sxs-lookup"><span data-stu-id="3d502-493">Berns\[1\]: Berns, *Billmeyer and Saltzman's Principles of Color Technology*, 3 <sub>rd</sub> Ed.</span></span> <span data-ttu-id="3d502-494">John Wiley & hijos (2000).</span><span class="sxs-lookup"><span data-stu-id="3d502-494">John Wiley & Sons (2000).</span></span>

<span data-ttu-id="3d502-495">Berna \[ 2 \] : bernas y Katoh, la función de transferencia digital a radiométrica para monitores de CRT controlados por el equipo, *estándares de color de CIE Expert Symposium ' 97 para la tecnología de creación de imágenes*, noviembre de 1997.</span><span class="sxs-lookup"><span data-stu-id="3d502-495">Berns\[2\]: Berns and Katoh, The digital to radiometric transfer function for computer controlled CRT displays, *CIE Expert Symposium '97 Colour Standards for Imaging Technology*, Nov. 1997.</span></span>

<span data-ttu-id="3d502-496">Berna \[ 3 \] : bernas, Fernandez y TAPLIN, estimación de Black-Level emisiones de Computer-Controlled muestra, *investigación de color y aplicación*, 28:379-383 Wiley periódicamente, Inc. (2003)</span><span class="sxs-lookup"><span data-stu-id="3d502-496">Berns\[3\]: Berns, Fernandez and Taplin, Estimating Black-Level Emissions of Computer-Controlled Displays, *Color Research and Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)</span></span>

<span data-ttu-id="3d502-497">Kang \[ 1 \] : Kang, *tecnología de color para dispositivos de imágenes electrónicas*, SPIE (1997)</span><span class="sxs-lookup"><span data-stu-id="3d502-497">Kang\[1\]: Kang, *Color Technology for Electronic Imaging Devices*, SPIE (1997)</span></span>

<span data-ttu-id="3d502-498">Katoh \[ 1 \] : Katoh, Deguchi y Berna, una caracterización precisa de la propuesta de monitor de CRT (II) para una extensión al método CIE y su comprobación, *OPT. Rev.* 8:397-408 (2001)</span><span class="sxs-lookup"><span data-stu-id="3d502-498">Katoh\[1\]: Katoh, Deguchi and Berns, An accurate characterization of CRT monitor (II) proposal for an extension to CIE method and its verification, *Opt. Rev.* 8: 397-408 (2001)</span></span>

### <a name="lcd-device-model-baseline"></a><span data-ttu-id="3d502-499">Línea de base del modelo de dispositivo LCD</span><span class="sxs-lookup"><span data-stu-id="3d502-499">LCD Device Model Baseline</span></span>

<span data-ttu-id="3d502-500">La línea de base del modelo de dispositivo LCD es similar a la línea base del modelo de dispositivo CRT.</span><span class="sxs-lookup"><span data-stu-id="3d502-500">The LCD Device Model Baseline is similar to the CRT Device Model Baseline.</span></span> <span data-ttu-id="3d502-501">En esta sección se explican las formas en que el modelado de LCD difiere del modelado de CRT.</span><span class="sxs-lookup"><span data-stu-id="3d502-501">This section will explain the ways in which LCD modeling differs from CRT modeling.</span></span>

<span data-ttu-id="3d502-502">Una diferencia es que no se puede suponer que las pantallas LCD siguen el modelo GOG que se usa para los CRT, y las curvas de tono se obtienen mediante la interpolación de los datos medidos.</span><span class="sxs-lookup"><span data-stu-id="3d502-502">One difference is that you cannot assume that LCD displays follow the GOG model used for CRTs, and the tone curves are obtained by interpolation of measured data.</span></span> <span data-ttu-id="3d502-503">Por eso, el eje neutro del dispositivo debe muestrearse con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="3d502-503">Because of that, the device neutral axis should be sampled more frequently.</span></span>

<span data-ttu-id="3d502-504">Estos son algunos valores de ejemplo típicos que pueden generar buenos datos para la línea de base del modelo de dispositivo LCD:</span><span class="sxs-lookup"><span data-stu-id="3d502-504">Here are some typical example values that can generate good data for the LCD device model baseline:</span></span>

<span data-ttu-id="3d502-505">Rojo: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-505">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="3d502-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="3d502-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="3d502-508">Neutros: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span><span class="sxs-lookup"><span data-stu-id="3d502-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span></span>

<span data-ttu-id="3d502-509">El proceso de calcular el promedio de los colores de color medidos para obtener las cromacidads de las principales del dispositivo es más importante para los monitores de LCD que para los CRT.</span><span class="sxs-lookup"><span data-stu-id="3d502-509">The process of averaging measured color chromaticies to obtain the chromaticities for the device primaries is more critical for LCDs than it is for CRTs.</span></span> <span data-ttu-id="3d502-510">Cuando las medidas XYZ se representan en el plano *XY* de cromaticidad, se muestra una situación típica en la figura 1.</span><span class="sxs-lookup"><span data-stu-id="3d502-510">When XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="3d502-511">Observe cómo se desplaza la cromaticidad hacia el punto negro.</span><span class="sxs-lookup"><span data-stu-id="3d502-511">Notice how the chromaticity drifts toward the black point.</span></span> <span data-ttu-id="3d502-512">Esto se debe a que todas las pantallas LCD tienen una cierta cantidad de fugas ligeras.</span><span class="sxs-lookup"><span data-stu-id="3d502-512">This is because all LCDs have a certain amount of light leakage.</span></span>

![Diagrama que muestra un gráfico de la cromaticidad usando datos sin procesar sin corrección.](images/cdmp-lcd-dmp-figure1.png)

<span data-ttu-id="3d502-514">**Figura 1** : Diagrama de cromaticidad con datos sin procesar sin corrección</span><span class="sxs-lookup"><span data-stu-id="3d502-514">**Figure 1** : The chromaticity diagram using raw data with no correction</span></span>

<span data-ttu-id="3d502-515">Cuando se resta de las medidas de XYZ sin procesar, se muestra una situación típica en la figura 2.</span><span class="sxs-lookup"><span data-stu-id="3d502-515">When this is subtracted from the raw XYZ measurements, a typical situation is depicted in Figure 2.</span></span> <span data-ttu-id="3d502-516">Ahora, los puntos están agrupados en clústeres de tres centros, aunque no son idénticos en ellos.</span><span class="sxs-lookup"><span data-stu-id="3d502-516">Tthe points are now clustered about three centers, although they don't fall identically on them.</span></span> <span data-ttu-id="3d502-517">El proceso de promedio descrito para los CRT mejora en gran medida los resultados de las pantallas LCD.</span><span class="sxs-lookup"><span data-stu-id="3d502-517">The averaging process described for CRTs greatly improves the results for LCDs.</span></span>

![Diagrama que muestra un gráfico de la cromaticidad usando datos sin procesar con un punto negro ajustado.](images/cdmp-lcd-dmp-figure2.png)

<span data-ttu-id="3d502-519">**Figura 2** : el diagrama de cromaticidad con datos con el punto negro ajustado</span><span class="sxs-lookup"><span data-stu-id="3d502-519">**Figure 2** : The chromaticity diagram using data with adjusted black point</span></span>

### <a name="rgb-capture-device-model-baseline"></a><span data-ttu-id="3d502-520">Línea de base del modelo de dispositivo de captura RGB</span><span class="sxs-lookup"><span data-stu-id="3d502-520">RGB Capture Device Model Baseline</span></span>

<span data-ttu-id="3d502-521">El modelo de dispositivo de captura RGB de línea base es una subclase de la clase IDeviceModel.</span><span class="sxs-lookup"><span data-stu-id="3d502-521">The baseline RGB capture device model is a subclass of the IDeviceModel class.</span></span> <span data-ttu-id="3d502-522">En la caracterización colorimétrica de los dispositivos de captura de color, como los escáneres y las cámaras digitales, se usa el enfoque siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d502-522">In the colorimetric characterization of color capture devices, such as scanners and digital cameras, the following approach is used.</span></span> <span data-ttu-id="3d502-523">Un destino compuesto por revisiones de color con valores de CIEXYZ conocidos se captura mediante el dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="3d502-523">A target consisting of color patches with known CIEXYZ values is captured using the capture device.</span></span> <span data-ttu-id="3d502-524">El resultado de la captura es una imagen de mapa de bits RGB en la que el color de cada revisión se codifica en un valor RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-524">The result of the capture is an RGB bitmap image in which the color of each patch is encoded in an RGB value.</span></span> <span data-ttu-id="3d502-525">Estos valores RGB de dispositivo son específicos de un dispositivo de captura determinado.</span><span class="sxs-lookup"><span data-stu-id="3d502-525">These device RGB values are specific to a particular capture device.</span></span> <span data-ttu-id="3d502-526">El objetivo de la caracterización colorimétrica es establecer una relación empírica entre los valores RGB del dispositivo y los valores CIEXYZ, o una transformación matemática de RGB a XYZ que se modele de la forma más precisa posible del comportamiento del dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="3d502-526">The goal of colorimetric characterization is to establish an empirical relationship between the device RGB values and CIEXYZ values, or a mathematical transformation from RGB to XYZ that models as accurately as possible the behavior of the capture device.</span></span>

<span data-ttu-id="3d502-527">Este tipo de transformación matemática se puede modelar razonablemente mediante polinomiales de bajo grado.</span><span class="sxs-lookup"><span data-stu-id="3d502-527">Such a mathematical transformation can be modeled reasonably by polynomials of low degrees.</span></span> <span data-ttu-id="3d502-528">Este procedimiento se detalla en la literatura, por ejemplo, Kang \[ 92 \] , Kang \[ 97 \] .</span><span class="sxs-lookup"><span data-stu-id="3d502-528">This procedure is detailed in the literature, for example Kang\[92\], Kang\[97\].</span></span> <span data-ttu-id="3d502-529">En Kang \[ 97 \] , se genera un enfoque que utiliza un conjunto de tres polinómicas con 3, 6, 8, 9, 11, 14 o 20 términos en las variables R, G y B, mientras que las tres regresión polinómicas están respectivamente en los componentes X, Y y Z del espacio CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="3d502-529">In Kang\[97\], an approach is reported that uses a set of three polynomials with 3, 6, 8, 9, 11, 14 or 20 terms in the R, G, and B variables, while the three polynomials regress respectively into the X, Y, Z components of the CIEXYZ space.</span></span> <span data-ttu-id="3d502-530">En el caso de la Polinómico de 20 términos, el formulario es:</span><span class="sxs-lookup"><span data-stu-id="3d502-530">For the 20-term polynomial, the form is:</span></span>

![Muestra el Polinómico de 20 términos.](images/cdmp-formula20.png)

<span data-ttu-id="3d502-532">Hay expresiones similares para y y Z. La técnica matemática para ajustar los polinómicos se encuentra dentro de "regresión lineal multivariada" y se describe en cualquier texto elemental en las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="3d502-532">There are similar expressions for Y and Z. The mathematical technique for fitting the polynomials falls within "Multivariate Linear Regression" and is described in any elementary text in Statistics.</span></span>

<span data-ttu-id="3d502-533">Este método de regresión lineal sufre que no se minimice la función de objetivo "derecho".</span><span class="sxs-lookup"><span data-stu-id="3d502-533">This method of linear regression suffers from not minimizing the "right" objective function.</span></span> <span data-ttu-id="3d502-534">Por diseño, la regresión lineal encuentra la solución de los mínimos cuadrados, lo que implica que los coeficientes obtenidos reducirán la suma total de los cuadrados de los errores en el espacio subyacente, o equivalentes, la suma de los cuadrados de las distancias euclidiana.</span><span class="sxs-lookup"><span data-stu-id="3d502-534">By design, linear regression finds the least squares solution, which implies that the coefficients obtained will minimize the total sum of squares of errors in the underlying space, or equivalently, the sum of squares of the Euclidean distances.</span></span> <span data-ttu-id="3d502-535">En la práctica, desea minimizar la suma de los cuadrados de? Es, ¿dónde? E es uno de los estándares aceptados, como CIE94.</span><span class="sxs-lookup"><span data-stu-id="3d502-535">In practice, you want to minimize the sum of squares of ?Es, where ?E is one of the accepted standards such as CIE94.</span></span> <span data-ttu-id="3d502-536">Minimizar esta función de objetivo es un problema de regresión no lineal.</span><span class="sxs-lookup"><span data-stu-id="3d502-536">Minimizing this objective function is a nonlinear regression problem.</span></span>

<span data-ttu-id="3d502-537">En el nuevo motor, Lab to XYZ es el espacio de colores CIE en el que se retrasan y se usa el polinomial cúbico de 20 términos como modelo para el dispositivo de captura, o coeficientes LS, como, como BS, de modo que las siguientes polinomias minimicen la suma de los cuadrados de? E <sub>CIE94</sub> s.</span><span class="sxs-lookup"><span data-stu-id="3d502-537">In the new engine, Lab to XYZ is the CIE color space that is regressed into, and the 20-term cubic polynomial is used as the model for the capture device, or coefficients ls,as,bs such that the following polynomials minimize the sum of squares of ?E <sub>CIE94</sub> s.</span></span>

![Muestra un conjunto de fórmulas polinómicas.](images/cdmp-formula21.png)

<span data-ttu-id="3d502-539">La solución ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) en el espacio numérico real de la dimensión 60 **R** 203 debe ser tal que se minimice el siguiente error total:</span><span class="sxs-lookup"><span data-stu-id="3d502-539">The solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) in the 60-dimensional real numeric space **R** 203 must be such that the following total error is minimized:</span></span>

![Muestra el error total que se va a minimizar.](images/cdmp-formula22.png)

<span data-ttu-id="3d502-541">donde la suma se realiza a través de todos los pares de puntos de datos (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) en el conjunto de datos muestreado, además de los puntos de control adicionales que se detallan a continuación.</span><span class="sxs-lookup"><span data-stu-id="3d502-541">where the summation is through all the data point pairs (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v<sub>i</sub>* ) in the sampled data set plus additional control points to be detailed in the following.</span></span> <span data-ttu-id="3d502-542">Se trata de un problema de regresión no lineal porque los parámetros *?<sub> i</sub>*, *<sub>i</sub>*, \* <sub>i</sub>\* entrar en la función de objetivo de una manera no lineal (no es cuadrática).</span><span class="sxs-lookup"><span data-stu-id="3d502-542">This is a nonlinear regression problem because the parameters *?<sub>i</sub>*, *a<sub>i</sub>*, \* <sub>i</sub>\* enter into the objective function in a nonlinear way (not quadratically).</span></span>

<span data-ttu-id="3d502-543">Dado que la función de objetivos</span><span class="sxs-lookup"><span data-stu-id="3d502-543">Because the objective function ?</span></span> <span data-ttu-id="3d502-544">¿es una función no lineal (y no cuadrática) de los parámetros *?<sub> i</sub>*, *<sub>i</sub>* y \* <sub>i</sub>\*, debe recurrir a técnicas iterativas para solucionar el problema de optimización.</span><span class="sxs-lookup"><span data-stu-id="3d502-544">is a nonlinear (and nonquadratic) function of the parameters *?<sub>i</sub>*, *a<sub>i</sub>* and \* <sub>i</sub>\*, you must resort to iterative techniques to solve the optimization problem.</span></span> <span data-ttu-id="3d502-545">Dado que la forma de la función Objective es una suma de cuadrados, se usa una técnica de optimización estándar denominada algoritmo Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="3d502-545">Because the form of the objective function is a sum of squares, a standard optimization technique called the Levenberg-Marquardt algorithm is used.</span></span> <span data-ttu-id="3d502-546">Se considera el método preferido para los problemas con menos líneas de cuadrados.</span><span class="sxs-lookup"><span data-stu-id="3d502-546">It is considered the method of choice for nonlinear least squares problems.</span></span> <span data-ttu-id="3d502-547">Para los algoritmos iterativos como Levenberg-Marquardt, debe proporcionar una estimación inicial.</span><span class="sxs-lookup"><span data-stu-id="3d502-547">For iterative algorithms such as Levenberg-Marquardt, you must supply an initial guess.</span></span> <span data-ttu-id="3d502-548">Una buena estimación inicial suele ser fundamental para buscar el valor mínimo correcto.</span><span class="sxs-lookup"><span data-stu-id="3d502-548">A good initial guess is usually critical in finding the correct minimum value.</span></span> <span data-ttu-id="3d502-549">En este caso, una buena candidata para la estimación inicial es la solución del problema de regresión lineal.</span><span class="sxs-lookup"><span data-stu-id="3d502-549">In this case, one good candidate for the initial guess is the solution of the linear regression problem.</span></span> <span data-ttu-id="3d502-550">En primer lugar, minimice la suma del cuadrado de las distancias de euclidiana en el espacio de laboratorio, definiendo una función de objetivo cuadrático:</span><span class="sxs-lookup"><span data-stu-id="3d502-550">First, minimize the sum of the square of Euclidean distances in Lab space, by defining a quadratic objective function:</span></span>

![Muestra una función de objetivo cuadrático definida.](images/cdmp-formula23.png)

<span data-ttu-id="3d502-552">La solución matemática a este problema de "mínimos cuadrados lineales" es muy conocida.</span><span class="sxs-lookup"><span data-stu-id="3d502-552">The mathematical solution to such "linear least squares" problem is well known.</span></span> <span data-ttu-id="3d502-553">Porque *?<sub></sub>solo aparece* en el modelado *L* , solo aparece en el modelado *u* *, y <sub></sub>* \* <sub>i</sub>\* solo aparece en el modelado *v* ; el problema de optimización se puede descomponer en tres subproblemas: uno para *L*, uno para *u* y otro para *v*.</span><span class="sxs-lookup"><span data-stu-id="3d502-553">Because *?<sub>i</sub>* only appears in the *L* modeling, *a <sub>i</sub>* only appears in the *u* modeling, and \* <sub>i</sub>\* only appears in the *v* modeling; the optimization problem can be decomposed into three subproblems: one for *L*, one for *u* and one for *v*.</span></span> <span data-ttu-id="3d502-554">Considere las ecuaciones *L* .</span><span class="sxs-lookup"><span data-stu-id="3d502-554">Consider the *L* equations.</span></span> <span data-ttu-id="3d502-555">(Las ecuaciones *u* y las ecuaciones *v* siguen exactamente el mismo argumento). El problema de minimizar la suma de los cuadrados de los errores en *L* puede indicarse como resolver la siguiente ecuación de matriz en el sentido de los mínimos cuadrados:</span><span class="sxs-lookup"><span data-stu-id="3d502-555">(The *u* equations and the *v* equations follow exactly the same argument.) The problem of minimizing the sum of squares of errors in *L* can be stated as solving the following matrix equation in the least squares sense:</span></span>

![Muestra una ecuación de matriz para L.](images/cdmp-formula24.png)

<span data-ttu-id="3d502-557">donde *N* es el número total de puntos de datos (puntos muestreados originales más puntos de control creados de la manera que se describe a continuación).</span><span class="sxs-lookup"><span data-stu-id="3d502-557">where *N* is the total number of data points (original sampled points plus control points created in a manner described below).</span></span> <span data-ttu-id="3d502-558">Normalmente, *N* es mucho mayor que 20, por lo que se determina la ecuación anterior, lo que requiere una solución con menos cuadrados.</span><span class="sxs-lookup"><span data-stu-id="3d502-558">Typically, *N* is much larger than 20, so the preceding equation is over-determined, requiring a least squares solution.</span></span> <span data-ttu-id="3d502-559">Una solución de formulario cerrado para **?**</span><span class="sxs-lookup"><span data-stu-id="3d502-559">A closed form solution for **?**</span></span> <span data-ttu-id="3d502-560">está disponible:</span><span class="sxs-lookup"><span data-stu-id="3d502-560">is available:</span></span>

![Muestra una solución de formulario cerrada.](images/cdmp-formula25.png)

<span data-ttu-id="3d502-562">En la práctica, no se usa la evaluación directa mediante la solución de formulario cerrado porque tiene propiedades numéricas deficientes.</span><span class="sxs-lookup"><span data-stu-id="3d502-562">In practice, direct evaluation using the closed form solution is not used because it has poor numerical properties.</span></span> <span data-ttu-id="3d502-563">En su lugar, se aplica un tipo de algoritmo de factorización de matriz a la matriz de coeficientes, lo que reduce el sistema de ecuaciones a un formato canónico.</span><span class="sxs-lookup"><span data-stu-id="3d502-563">Instead, some kind of matrix factorization algorithm is applied to the coefficient matrix which reduces the system of equations to a canonical form.</span></span> <span data-ttu-id="3d502-564">En la implementación actual, se aplica la descomposición de valores singular (SVD) a la matriz **R** y, a continuación, se resuelve el sistema descompuesto resultante.</span><span class="sxs-lookup"><span data-stu-id="3d502-564">In the current implementation, Singular Value Decomposition (SVD) is applied to the matrix **R** and then the resulting decomposed system is solved.</span></span>

<span data-ttu-id="3d502-565">La solución al problema de regresión lineal, indicada por ![ muestra la solución al problema de regresión lineal.](images/cdmp-formula26.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-565">The solution to the linear regression problem, denoted by ![Shows the solution to the linear regression problem.](images/cdmp-formula26.png)</span></span> <span data-ttu-id="3d502-566">, se usa como punto inicial del algoritmo Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="3d502-566">, is used as the starting point of the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="3d502-567">En este algoritmo, se calcula un paso de prueba que debe ir más cerca de la solución óptima.</span><span class="sxs-lookup"><span data-stu-id="3d502-567">In this algorithm, a trial step is computed that should move the point closer to the optimal solution.</span></span> <span data-ttu-id="3d502-568">El paso de prueba satisface un conjunto de ecuaciones lineales que dependen del valor funcional y de los valores de los derivados en el punto actual.</span><span class="sxs-lookup"><span data-stu-id="3d502-568">The trial step satisfies a set of linear equations dependent on the functional value and values of the derivatives at the current point.</span></span> <span data-ttu-id="3d502-569">Por esta razón, los derivados de la función Objective?</span><span class="sxs-lookup"><span data-stu-id="3d502-569">For this reason, the derivatives of the objective function ?</span></span> <span data-ttu-id="3d502-570">¿con respecto a los parámetros *?<sub> i</sub>*, *se <sub></sub> <sub></sub>* necesitan entradas para el algoritmo de Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="3d502-570">with respect to the parameters *?<sub>i</sub>*, *a<sub>i</sub> <sub>i</sub>* are required inputs to the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="3d502-571">Aunque hay 60 parámetros, hay un acceso directo que le permite calcular mucho menos.</span><span class="sxs-lookup"><span data-stu-id="3d502-571">Although there are 60 parameters, there is a shortcut that allows you to compute a lot less.</span></span> <span data-ttu-id="3d502-572">Por la regla de cadena de cálculo,</span><span class="sxs-lookup"><span data-stu-id="3d502-572">By the Chain Rule of Calculus,</span></span>

![Muestra una ecuación que permite usar un acceso directo mediante la regla de cadena de cálculo.](images/cdmp-formula27.png)

<span data-ttu-id="3d502-574">donde *j* = 1, 2, 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* es el valor CIELab del punto de ejemplo *i* TH y *r <sub>ij</sub>* es la entrada (*i*,*j* ) de la matriz **R** definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3d502-574">where *j* = 1, 2,  , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* are the CIELAB value of the *i* th sample point, and *R <sub>ij</sub>* is the (*i*,*j* )th entry of the matrix **R** defined above.</span></span> <span data-ttu-id="3d502-575">Por lo tanto, en lugar de calcular los derivados para los parámetros 60, puede calcular los derivados de *L*,*a* y *b* mediante la diferencia de avance numérica.</span><span class="sxs-lookup"><span data-stu-id="3d502-575">So instead of computing derivatives for 60 parameters, you can compute derivatives for *L*,*a*, and *b* using numerical forward differencing.</span></span>

<span data-ttu-id="3d502-576">También es necesario configurar un criterio de detención para los algoritmos iterativos.</span><span class="sxs-lookup"><span data-stu-id="3d502-576">It is also necessary to set up a stopping criterion for iterative algorithms.</span></span> <span data-ttu-id="3d502-577">En la implementación actual, las iteraciones se terminan si el DECIE94 cuadrado medio es menor que 1, o el número de iteraciones realizadas ha superado 10.</span><span class="sxs-lookup"><span data-stu-id="3d502-577">In the current implementation, the iterations are terminated if the mean square DECIE94 is less than 1, or the number of iterations performed has exceeded 10.</span></span> <span data-ttu-id="3d502-578">El número 10 procede de la experiencia práctica de que, si las primeras iteraciones no reducen el error de forma significativa, las iteraciones posteriores no ayudarán a evitar que se mueva el punto de una manera oscilante, es decir, el algoritmo no puede converger.</span><span class="sxs-lookup"><span data-stu-id="3d502-578">The number 10 comes from the practical experience that if the first few iterations do not reduce the error significantly, further iterations would not help much other than moving the point in an oscillatory manner, i.e., the algorithm may not converge.</span></span> <span data-ttu-id="3d502-579">Incluso en el caso de que el algoritmo difiera, podemos estar seguros de que el DECIE94 no es peor que lo que iniciamos, es decir, con los parámetros obtenidos de la regresión lineal.</span><span class="sxs-lookup"><span data-stu-id="3d502-579">Even in the case that the algorithm diverges, we can be sure that the DECIE94 is no worse than what we started, i.e. with the parameters obtained from linear regression.</span></span>

<span data-ttu-id="3d502-580">Incluso con el método anterior de regresión no lineal, hay varios problemas con la conexión.</span><span class="sxs-lookup"><span data-stu-id="3d502-580">Even with the preceding method of nonlinear regression, there are several problems with the fitting.</span></span> <span data-ttu-id="3d502-581">Uno de los problemas es que los polinómicos tienden a sobrepasar o a superar los puntos de datos.</span><span class="sxs-lookup"><span data-stu-id="3d502-581">One problem is that the polynomials tend to overshoot or undershoot beyond the data points.</span></span> <span data-ttu-id="3d502-582">Es posible que se introduzcan los máximos y mínimos artificiales en el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="3d502-582">Artificial local maxima and minima may be introduced in the fitting process.</span></span> <span data-ttu-id="3d502-583">Esto se puede compensar mediante el uso de polinomiales de bajo grado, que es el motivo por el que no debe usar más de tres grados.</span><span class="sxs-lookup"><span data-stu-id="3d502-583">This can be counteracted by using polynomials of low degree, which is the reason you should not use higher than three degrees.</span></span> <span data-ttu-id="3d502-584">Un aspecto más grave del exceso o el subintento es que, mientras que un polinomio puede tomar cualquier valor real teóricamente, el espacio que intenta modelar normalmente tiene restricciones físicas y restricciones prácticas.</span><span class="sxs-lookup"><span data-stu-id="3d502-584">A more serious aspect of overshooting or undershooting is that, while a polynomial can take any real value theoretically, the space it tries to model typically has physical constraints and practical constraints.</span></span> <span data-ttu-id="3d502-585">CIEXYZ debe tener todos los valores X, Y, Z no negativos, que es una restricción física.</span><span class="sxs-lookup"><span data-stu-id="3d502-585">CIEXYZ must have all of X, Y, Z non-negative, which is a physical constraint.</span></span> <span data-ttu-id="3d502-586">En la práctica, solo toman valores en la magnitud de cientos, no en miles o más.</span><span class="sxs-lookup"><span data-stu-id="3d502-586">In practice, they only take values in the magnitude of hundreds, not thousands or higher.</span></span> <span data-ttu-id="3d502-587">Del mismo modo, CIELAB o CIELUV tiene sus propias restricciones físicas y prácticas.</span><span class="sxs-lookup"><span data-stu-id="3d502-587">Similarly, CIELAB or CIELUV has its own physical and practical constraints.</span></span> <span data-ttu-id="3d502-588">Cuando el espacio RGB se rellena con puntos de ejemplo, el problema de un exceso o un subgrave no es serio.</span><span class="sxs-lookup"><span data-stu-id="3d502-588">When the RGB space is filled sufficiently with sample points, the problem of overshooting or undershooting is not serious.</span></span> <span data-ttu-id="3d502-589">Sin embargo, los puntos RGB capturados desde el dispositivo de captura no suelen llenar el espacio RGB de manera uniforme.</span><span class="sxs-lookup"><span data-stu-id="3d502-589">However, the captured RGB points from the capture device do not usually fill up the RGB space uniformly.</span></span> <span data-ttu-id="3d502-590">Los puntos solo pueden rellenar el 80% del cubo RGB, o peor, pueden residir en un conjunto de un conjunto de dimensiones inferior.</span><span class="sxs-lookup"><span data-stu-id="3d502-590">The points may fill up only inner the 80% of the RGB cube, or worse, they may reside in a lower dimensional manifold.</span></span> <span data-ttu-id="3d502-591">Cuando esto sucede, los polinómicos con regresión pueden hacer un trabajo pobre en la extrapolación de los valores más allá de los puntos de datos, a veces devolviendo predicciones no reareales.</span><span class="sxs-lookup"><span data-stu-id="3d502-591">When this happens, the regressed polynomials may do a poor job at extrapolating the values beyond the data points, sometimes returning unrealistic predictions.</span></span> <span data-ttu-id="3d502-592">Desea un modelo que siempre devuelva valores realistas razonablemente.</span><span class="sxs-lookup"><span data-stu-id="3d502-592">You want a model that always returns reasonably realistic values.</span></span> <span data-ttu-id="3d502-593">Esto requiere un método que pueda controlar eficazmente el comportamiento del límite de los polinómicos de regresión imponiendo costos adicionales a esos polinómicos que se comportan de forma errática cerca del límite del cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-593">This requires a method that can effectively control the boundary behavior of regression polynomials by imposing additional cost to those polynomials that behave erratically near the boundary of the RGB cube.</span></span> <span data-ttu-id="3d502-594">Una medida adicional para asegurarse de que los polinomiales siempre devuelven valores realistas se aplican recortando la salida a dentro del raíz espectral de CIE.</span><span class="sxs-lookup"><span data-stu-id="3d502-594">A further measure to ensure that the polynomials always return realistic values is applied by clipping the output to within the CIE spectral locus.</span></span>

<span data-ttu-id="3d502-595">En este punto, el modelado del escáner y el modelado de la cámara difieren entre sí.</span><span class="sxs-lookup"><span data-stu-id="3d502-595">It is at this point that the scanner modeling and camera modeling diverge from each other.</span></span> <span data-ttu-id="3d502-596">Se espera que el modelo de cámara se extrapola a regiones más allá de los puntos muestreados, incluido el "reflejos especulares", la misma extrapolación no es necesaria para el modelo de escáner.</span><span class="sxs-lookup"><span data-stu-id="3d502-596">The camera model is expected to extrapolate to regions beyond the sampled points including the "specular highlights," the same extrapolation is not required for the scanner model.</span></span> <span data-ttu-id="3d502-597">Se espera que el destino del escáner cubra una caracterización similar a la de los materiales impresos que se van a examinar.</span><span class="sxs-lookup"><span data-stu-id="3d502-597">The scanner target is expected to cover a characterization that is similar to the printed materials to be scanned.</span></span> <span data-ttu-id="3d502-598">Todavía es necesario que el modelo del escáner sea robusto en el sentido de que no debe devolver valores no reales, pero no se requiere la extrapolación más allá del destino de la caracterización.</span><span class="sxs-lookup"><span data-stu-id="3d502-598">The scanner model is still required to be robust in the sense that it should not return unrealistic values, but extrapolation far beyond the characterization target is not required.</span></span> <span data-ttu-id="3d502-599">Para garantizar la solidez, la L polinómica anterior se recorta en 100, es decir, el modelo Polinómico se fuerza a no extrapolar más allá de "DMín" del destino del escáner.</span><span class="sxs-lookup"><span data-stu-id="3d502-599">To ensure robustness, the L-polynomial above is clipped at 100, that is, the polynomial model is forced not to extrapolate beyond "Dmin" of the scanner target.</span></span>

<span data-ttu-id="3d502-600">Se espera que el modelo de cámara se extrapolar a las iluminaciones especulares, por lo que no se desea recortar en 100.</span><span class="sxs-lookup"><span data-stu-id="3d502-600">The camera model is expected to extrapolate to specular highlights, so clipping at 100 is undesirable.</span></span> <span data-ttu-id="3d502-601">En su lugar, se utiliza el algoritmo siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d502-601">Instead, the following algorithm is used.</span></span>

<span data-ttu-id="3d502-602">Los puntos de control artificiales se introducen para controlar el comportamiento de los polinómicos en regiones con un muestreo insuficiente.</span><span class="sxs-lookup"><span data-stu-id="3d502-602">Artificial control points are introduced to control the behavior of the polynomials in regions with insufficient sampling.</span></span> <span data-ttu-id="3d502-603">Mediante la colocación estratégica de estos puntos de control con los valores adecuados, sirven para "extraer" los polinómicos en la dirección requerida.</span><span class="sxs-lookup"><span data-stu-id="3d502-603">By strategically placing these control points with appropriate values, they serve to "pull" the polynomials in the required direction.</span></span> <span data-ttu-id="3d502-604">En la implementación actual, se usan ocho puntos de control correspondientes a las esquinas del cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-604">In the current implementation, eight control points corresponding to the corners of the RGB cube are used.</span></span> <span data-ttu-id="3d502-605">Si los valores del dispositivo se normalizan en Unity, estos puntos son:</span><span class="sxs-lookup"><span data-stu-id="3d502-605">If the device values are normalized to unity, then these points are:</span></span>

<span data-ttu-id="3d502-606">*R* = 0, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-606">*R* = 0, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="3d502-607">*R* = 0, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="3d502-607">*R* = 0, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="3d502-608">*R* = 0, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-608">*R* = 0, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="3d502-609">*R* = 0.</span><span class="sxs-lookup"><span data-stu-id="3d502-609">*R* = 0.</span></span> <span data-ttu-id="3d502-610">*G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="3d502-610">*G* = 1, *B* = 1</span></span>

<span data-ttu-id="3d502-611">*R* = 1, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-611">*R* = 1, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="3d502-612">*R* = 1, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="3d502-612">*R* = 1, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="3d502-613">*R* = 1, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="3d502-613">*R* = 1, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="3d502-614">*R* = 1, *G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="3d502-614">*R* = 1, *G* = 1, *B* = 1</span></span>

<span data-ttu-id="3d502-615">Excepto en el caso de *R*  = *G*  = *p* = 1 blanco que está asociado a un valor CIELAB de *L* = 100, *u*  = *v* = 0, se usa el algoritmo de extrapolación siguiente para determinar el valor de CIELab adecuado con el que se va a asociar.</span><span class="sxs-lookup"><span data-stu-id="3d502-615">Except for the white *R* =*G* =*B* = 1, which is associated with a CIELAB value of *L* = 100, *u* =*v* = 0, the following extrapolation algorithm is used to determine the appropriate CIELAB value to be associated with.</span></span> <span data-ttu-id="3d502-616">Por lo general, para un determinado (*r*,*g*,*b* ), se asocia una ponderación a cada uno de los (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ) del conjunto de datos muestreado.</span><span class="sxs-lookup"><span data-stu-id="3d502-616">Generally, for a given (*R*,*G*,*B* ), a weight is associated with each of the (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ) in the sampled data set.</span></span> <span data-ttu-id="3d502-617">Hay dos objetivos para asignar el peso.</span><span class="sxs-lookup"><span data-stu-id="3d502-617">There are two goals to assigning the weight.</span></span> <span data-ttu-id="3d502-618">En primer lugar, el peso es inversamente proporcional a la distancia entre (*r*,*G*,*B* ) y (*R <sub>i</sub>*,*G <sub>i</sub>*,*b <sub>i</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="3d502-618">First, the weight is inversely proportional to the distance between (*R*,*G*,*B* ) and (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ).</span></span> <span data-ttu-id="3d502-619">En segundo lugar, desea descartar o asignar el peso 0 a, los puntos que tienen un matiz diferente que el punto especificado (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="3d502-619">Second, you want to discard, or assign weight 0 to, points that have a different hue than the given point (*R*,*G*,*B* ).</span></span> <span data-ttu-id="3d502-620">Para tener en cuenta el matiz, considere los puntos que se encuentran dentro de un cono cuyo vértice está en (0,0), cuyo eje coincide con la línea que se une (0, 0,0) a (*R*,*G*,*B* ) y cuyo ángulo semivertical?</span><span class="sxs-lookup"><span data-stu-id="3d502-620">To take the hue into account, consider points that lie within a cone whose vertex is at (0, 0, 0), whose axis coincides with the line joining (0, 0, 0) to (*R*,*G*,*B* ), and whose semi-vertical angle ?</span></span> <span data-ttu-id="3d502-621">cumple los Co?</span><span class="sxs-lookup"><span data-stu-id="3d502-621">satisfies cos ?</span></span> <span data-ttu-id="3d502-622">= 0,9.</span><span class="sxs-lookup"><span data-stu-id="3d502-622">= 0.9.</span></span> <span data-ttu-id="3d502-623">Vea la figura 3 para ver una ilustración de este cono.</span><span class="sxs-lookup"><span data-stu-id="3d502-623">See Figure 3 for an illustration of this cone.</span></span>

![Diagrama que muestra la forma del entorno.](images/cdmp-lcd-dmp-figure3.png)

<span data-ttu-id="3d502-625">**Figura 3** : filtrado de los puntos de ejemplo por ángulo y distancia.</span><span class="sxs-lookup"><span data-stu-id="3d502-625">**Figure 3** : Filtering the sample points by angle and distance.</span></span> <span data-ttu-id="3d502-626">La forma del entorno representado solo es para fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="3d502-626">The shape of the neighborhood depicted is for illustration purpose only.</span></span> <span data-ttu-id="3d502-627">La forma real depende de la distancia utilizada. es un entorno en forma de rombo si se usa la norma 1.</span><span class="sxs-lookup"><span data-stu-id="3d502-627">The actual shape depends on the distance used; it is a diamond-shaped neighborhood if the 1-norm is used.</span></span>

<span data-ttu-id="3d502-628">Dentro de este cono, se realiza un segundo filtrado que se basa en la distancia RGB, que utiliza la norma 1, definida por</span><span class="sxs-lookup"><span data-stu-id="3d502-628">Within this cone, a second filtering is performed that is based on the RGB distance, which uses the 1-norm, defined by</span></span>

![Muestra la fórmula para el segundo filtrado dentro del cono.](images/cdmp-formula28.png)

<span data-ttu-id="3d502-630">Con el cono actual, la búsqueda inicial es para los puntos que se encuentran dentro de una distancia de 0,1 (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="3d502-630">With the current cone, the initial search is for points that are within a distance of 0.1 from (*R*,*G*,*B* ).</span></span> <span data-ttu-id="3d502-631">Si no se encuentra ningún punto dentro de este radio, el radio aumenta en 0,1 y la búsqueda se reinicia.</span><span class="sxs-lookup"><span data-stu-id="3d502-631">If no point is found within this radius, the radius is increased by 0.1, and the search is restarted.</span></span> <span data-ttu-id="3d502-632">Si en las siguientes redes de redondeo no hay ningún punto, el radio aumenta en 0,1.</span><span class="sxs-lookup"><span data-stu-id="3d502-632">If the next round nets no point either, the radius is increased by 0.1.</span></span> <span data-ttu-id="3d502-633">Este proceso continúa hasta que el radio supera MaxDist/5, donde MaxDist = 3, en el caso de 1-norma.</span><span class="sxs-lookup"><span data-stu-id="3d502-633">This process continues until the radius exceeds MaxDist/5, where MaxDist = 3, in the case of 1-norm.</span></span> <span data-ttu-id="3d502-634">Si no se encuentra ningún punto, el cono se amplía reduciendo la CES?</span><span class="sxs-lookup"><span data-stu-id="3d502-634">If no point is found, the cone is enlarged by decreasing the cos ?</span></span> <span data-ttu-id="3d502-635">por 0,05, es decir, al aumentar el ángulo?</span><span class="sxs-lookup"><span data-stu-id="3d502-635">by 0.05, that is, increasing the angle ?</span></span> <span data-ttu-id="3d502-636">y reinicie todo el proceso con un radio en aumento.</span><span class="sxs-lookup"><span data-stu-id="3d502-636">and restarting the whole process with an increasing radius.</span></span> <span data-ttu-id="3d502-637">Este proceso continúa hasta que se encuentra un conjunto de puntos no vacío o cos?</span><span class="sxs-lookup"><span data-stu-id="3d502-637">This process continues until a non-empty set of points is found, or cos ?</span></span> <span data-ttu-id="3d502-638">llega a 0, es decir, el cono se ha abierto hasta convertirse en un plano.</span><span class="sxs-lookup"><span data-stu-id="3d502-638">reaches 0, that is, the cone has opened up to become a plane.</span></span> <span data-ttu-id="3d502-639">En este punto, la búsqueda se reinicia aumentando el radio, salvo que la búsqueda continúa hasta que el radio llega a MaxDist.</span><span class="sxs-lookup"><span data-stu-id="3d502-639">At this point, the search is restarted by increasing the radius, except that the search continues until the radius reaches MaxDist.</span></span> <span data-ttu-id="3d502-640">Esto garantiza que, en el peor de los casos, se encontrará un conjunto de puntos no vacío.</span><span class="sxs-lookup"><span data-stu-id="3d502-640">This guarantees that in the worst-case scenario, a non-empty set of points will be found.</span></span> <span data-ttu-id="3d502-641">El algoritmo se resume en el diagrama de flujo de la figura 4.</span><span class="sxs-lookup"><span data-stu-id="3d502-641">The algorithm is summarized in the flow diagram in Figure 4.</span></span>

![Diagrama que muestra el flujo del algoritmo.](images/cdmp-lcd-dmp-figure4.png)

<span data-ttu-id="3d502-643">**Figura 4** : Diagrama de flujo para determinar los conjuntos de puntos de ejemplo usados en la extrapolación para un valor RGB de entrada</span><span class="sxs-lookup"><span data-stu-id="3d502-643">**Figure 4** : Flow diagram for determining the set S of sample points used in the extrapolation for an input RGB value</span></span>

<span data-ttu-id="3d502-644">Suponiendo que el proceso anterior produce *un conjunto de* puntos no vacíos (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) y el correspondiente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), para cada uno de estos puntos, se asigna una ponderación *w <sub></sub>* , proporcionada por</span><span class="sxs-lookup"><span data-stu-id="3d502-644">Assuming that the preceding process yields a non-empty set *S* of points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) and corresponding (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), then for each such point, a weight *w<sub>i</sub>* is assigned, given by</span></span>

![Muestra la fórmula para una ponderación de cada punto.](images/cdmp-formula29.png)

<span data-ttu-id="3d502-646">Por último, el extrapolant se define mediante</span><span class="sxs-lookup"><span data-stu-id="3d502-646">Finally, the extrapolant is defined by</span></span>

![Muestra la definición de extrapolant.](images/cdmp-formula30.png)

<span data-ttu-id="3d502-648">Las ecuaciones anteriores constituyen una instancia de los "métodos ponderados de distancia inversa", que normalmente se denominan métodos Charlene.</span><span class="sxs-lookup"><span data-stu-id="3d502-648">The preceding equations constitute an instance of the "inverse-distance weighted methods," commonly called the Shepard methods.</span></span> <span data-ttu-id="3d502-649">Al ejecutar cada uno de los ocho puntos de EQ (6) a través del algoritmo, se obtienen ocho puntos de control, cada uno con los valores *R*,*G*,*B* y *L*,*a* y *b* , que se colocan en el grupo con los datos de ejemplo originales.</span><span class="sxs-lookup"><span data-stu-id="3d502-649">By running each of the eight points from eq (6) through the algorithm, eight control points are obtained, each with *R*,*G*,*B* and *L*,*a*,*b* values, which are put into the pool with the original sample data.</span></span>

<span data-ttu-id="3d502-650">Para asegurarse de que el modelo siempre genera valores de color válidos y para la integridad del sistema y la estabilidad en toda la canalización de procesamiento de color, debe realizar un recorte final en la salida del modelo polinómico.</span><span class="sxs-lookup"><span data-stu-id="3d502-650">To ensure that the model always produces valid color values and for system integrity and stability down the whole color processing pipeline, you must perform a final clipping to the output of the polynomial model.</span></span> <span data-ttu-id="3d502-651">El componente achromatic (*y* o *L* ) y el componente cromático (*XY* o *a'b*, que están relacionados con el espacio XYZ mediante una transformación proyectada) describen la gama visual CIE.</span><span class="sxs-lookup"><span data-stu-id="3d502-651">The CIE visual gamut is described by the achromatic component (*Y* or *L* ) and the chromatic component (*xy* or *a'b'*, which are related to the XYZ space by a projective transformation).</span></span> <span data-ttu-id="3d502-652">En la implementación actual, se usa la cromaticidad de *a'b* porque está directamente relacionada con el espacio CIELUV.</span><span class="sxs-lookup"><span data-stu-id="3d502-652">In the current implementation, the *a'b'* chromaticity is used because it is directly related to the CIELUV space.</span></span> <span data-ttu-id="3d502-653">Para cualquier valor de *CIELAB* , primer clip *L* en un valor no negativo:</span><span class="sxs-lookup"><span data-stu-id="3d502-653">For any *CIELAB* value, first clip *L* to a non-negative value:</span></span>

![Muestra el recorte de L en un valor no negativo.](images/cdmp-formula31.png)

<span data-ttu-id="3d502-655">Para permitir la extrapolación de los reflejos especulares, *l* no se recorta en 100, el límite superior "convencional" para *L* en el espacio de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="3d502-655">To allow extrapolation for specular highlights, *L* is not clipped at 100, the "conventional" upper bound for *L* in Lab space.</span></span>

<span data-ttu-id="3d502-656">Después, si *L* = 0, a *y* *b* se recortan de modo que a *= b =* 0.</span><span class="sxs-lookup"><span data-stu-id="3d502-656">Next, if *L* = 0, then *a* and *b* are clipped such that a *= b =* 0.</span></span> <span data-ttu-id="3d502-657">Si es *L* ?</span><span class="sxs-lookup"><span data-stu-id="3d502-657">If *L* ?</span></span> <span data-ttu-id="3d502-658">0, calcular</span><span class="sxs-lookup"><span data-stu-id="3d502-658">0, calculate</span></span>

![Muestra la fórmula si L = 0.](images/cdmp-formula32.png)

<span data-ttu-id="3d502-660">Estos son los componentes de un vector en el diagrama de *a'b* desde el punto blanco (*u? '*,*v? '*</span><span class="sxs-lookup"><span data-stu-id="3d502-660">These are the components of a vector in the *a'b'* diagram from the white point (*u?'*,*v?'*</span></span> <span data-ttu-id="3d502-661">) al color en cuestión.</span><span class="sxs-lookup"><span data-stu-id="3d502-661">) to the color in question.</span></span> <span data-ttu-id="3d502-662">Defina el raíz espectral de CIE como el casco convexo de todos los puntos (*a '*,*b '* ), parametrizado por la longitud de onda?:</span><span class="sxs-lookup"><span data-stu-id="3d502-662">Define the CIE spectral locus as the convex hull of all the points (*a'*,*b'* ), parameterized by the wavelength ?:</span></span>

![Muestra la fórmula para la longitud de onda.](images/cdmp-formula33.png)

<span data-ttu-id="3d502-664">donde ![ muestra las funciones para la coincidencia de color de CIE.](images/cdmp-formula34.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-664">where ![Shows the functions for CIE color-matching.](images/cdmp-formula34.png)</span></span> <span data-ttu-id="3d502-665">son las funciones de coincidencia de color de CIE del observador de 2 grados.</span><span class="sxs-lookup"><span data-stu-id="3d502-665">are the CIE color-matching functions for the 2-degree observer.</span></span> <span data-ttu-id="3d502-666">Si el vector está fuera del raíz de CIE, el color se recorta hasta el punto en el raíz de CIE que es la intersección de raíz y la línea definida por el vector.</span><span class="sxs-lookup"><span data-stu-id="3d502-666">If the vector lies outside the CIE locus, the color is clipped to the point on the CIE locus that is the intersection of the locus and the line defined by the vector.</span></span> <span data-ttu-id="3d502-667">Vea la figura 5.</span><span class="sxs-lookup"><span data-stu-id="3d502-667">See Figure 5.</span></span> <span data-ttu-id="3d502-668">Si se ha producido un recorte, se reconstruye el valor *a* y *b* restando primero *a? '*</span><span class="sxs-lookup"><span data-stu-id="3d502-668">If clipping has occurred, the *a* and *b* value is reconstructed by first subtracting *a?'*</span></span> <span data-ttu-id="3d502-669">y *b? '*</span><span class="sxs-lookup"><span data-stu-id="3d502-669">and *b?'*</span></span> <span data-ttu-id="3d502-670">del recorte *a '* y *b '* y, a continuación, multiplicar por 13 *L*.</span><span class="sxs-lookup"><span data-stu-id="3d502-670">from the clipped *a'* and *b'*, and then multiplying by 13 *L*.</span></span>

![Diagrama que muestra el gráfico para el algoritmo de recorte.](images/cdmp-lcd-dmp-figure5.png)

<span data-ttu-id="3d502-672">**Figura 5** : algoritmo de recorte para los valores de laboratorio que se encuentran fuera de la gama visual de CIE</span><span class="sxs-lookup"><span data-stu-id="3d502-672">**Figure 5** : Clipping algorithm for Lab values that are outside the CIE visual gamut</span></span>

<span data-ttu-id="3d502-673">En la implementación actual, el raíz espectral de CIE en el plano *a'b* se representa mediante una curva lineal a trozos con segmentos 35 (que corresponde a una longitud de onda de 360 nm a 700 nm inclusive).</span><span class="sxs-lookup"><span data-stu-id="3d502-673">In the current implementation, the CIE spectral locus in the *a'b'* plane is represented by a piecewise linear curve with 35 segments (corresponding to a wavelength from 360 nm to 700 nm inclusive).</span></span> <span data-ttu-id="3d502-674">Mediante el orden de los segmentos de línea para que sus ángulos subpuestos en el punto blanco sean ascendentes, lo que equivale a las longitudes de onda descendentes, el segmento de línea que forma una intersección con el rayo formado por el vector anterior se puede encontrar mediante una búsqueda binaria simple.</span><span class="sxs-lookup"><span data-stu-id="3d502-674">By ordering the line segments so that their subtended angles at the white point are ascending, which is equivalent to descending wavelengths, the line segment that intersects with the ray formed by the above vector can be found by a simple binary search.</span></span>

### <a name="rgb-printer-device-model-baseline"></a><span data-ttu-id="3d502-675">Línea base del modelo de dispositivo de impresora RGB</span><span class="sxs-lookup"><span data-stu-id="3d502-675">RGB Printer Device Model Baseline</span></span>

<span data-ttu-id="3d502-676">Una caracterización de dispositivos de una impresora RGB consiste en construir un modelo empírico del dispositivo que predice el color CIELUV independiente del dispositivo para cualquier valor RGB determinado.</span><span class="sxs-lookup"><span data-stu-id="3d502-676">A device characterization of a RGB printer consists of constructing an empirical model of the device that predicts the device-independent CIELUV color for any given RGB value</span></span>

<span data-ttu-id="3d502-677">Hay dos maneras de construir el modelo empírico.</span><span class="sxs-lookup"><span data-stu-id="3d502-677">There are two ways to construct the empirical model.</span></span> <span data-ttu-id="3d502-678">Una manera es usar los datos del dispositivo para una impresora RGB y el otro es usar datos de parámetros analíticos.</span><span class="sxs-lookup"><span data-stu-id="3d502-678">One way is to use the device data for a RGB printer, and the other is to use analytical parameter data.</span></span> <span data-ttu-id="3d502-679">En el primero, los datos de medición proporcionados por un usuario para un dispositivo de impresora RGB se usan para crear una tabla de búsqueda en 3D (LUT).</span><span class="sxs-lookup"><span data-stu-id="3d502-679">In the first one, measurement data provided by a user for a RGB printer device is used to construct 3-D lookup table (LUT).</span></span> <span data-ttu-id="3d502-680">Los datos de medición se componen de valores XYZ para revisiones RGB muestreadas uniformemente.</span><span class="sxs-lookup"><span data-stu-id="3d502-680">The measurement data consists of XYZ values for uniformly sampled RGB patches.</span></span> <span data-ttu-id="3d502-681">Los tamaños de muestreo típicos son 9 o 17 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="3d502-681">Typical sampling sizes are 9 or 17 for each component.</span></span> <span data-ttu-id="3d502-682">Cada revisión se mide con un colorimeter o un espectrofotómetro en el espacio CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="3d502-682">Each patch is measured with a colorimeter or spectrophotometer in CIEXYZ space.</span></span> <span data-ttu-id="3d502-683">El valor XYZ para una revisión se convierte a continuación en el valor CIELUV, formando un LUT 3D.</span><span class="sxs-lookup"><span data-stu-id="3d502-683">The XYZ value for a patch is then converted into CIELUV value, forming a 3-D LUT.</span></span> <span data-ttu-id="3d502-684">En el modelo de dispositivo, el método de interpolación tetrahedral de Sakamoto se aplica a la LUT 3D para predecir los datos CIELUV para un dato RGB determinado.</span><span class="sxs-lookup"><span data-stu-id="3d502-684">In the device model, the Sakamoto's tetrahedral interpolation method is applied to the 3-D LUT in order to predict the CIELUV data for a given RGB data.</span></span> <span data-ttu-id="3d502-685">(Conviene la patente 4275413 de EE. UU. (Sakamoto et al.), patentes de EE. UU. 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="3d502-685">(Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="3d502-686">Las dos patentes mencionadas han expirado.).</span><span class="sxs-lookup"><span data-stu-id="3d502-686">The two patents mentioned have expired.).</span></span> <span data-ttu-id="3d502-687">Los datos de parámetros analíticos pasados en el segundo método son simplemente un LUT que se compiló anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3d502-687">The analytical parameter data passed in the second method is simply a LUT that was built previously.</span></span> <span data-ttu-id="3d502-688">Normalmente, la LUT se compiló con el primer método, aunque podría estar compilada a mano.</span><span class="sxs-lookup"><span data-stu-id="3d502-688">Typically, that LUT was built using the first method, although it could be hand-built.</span></span>

<span data-ttu-id="3d502-689">En la administración del color actual, el mapa de origen se define como la asignación que va desde el espacio RGB a un espacio de colores de CIEXYZ independiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d502-689">In the current color management, the source map is defined as the map that goes from RGB space to a device-independent CIEXYZ color space.</span></span> <span data-ttu-id="3d502-690">El mapa de destino se define como la asignación que va del espacio de colores CIEXYZ independiente del dispositivo al espacio RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-690">The destination map is defined as the map that goes from the device-independent CIEXYZ color space to RGB space.</span></span> <span data-ttu-id="3d502-691">Es el inverso del mapa de origen.</span><span class="sxs-lookup"><span data-stu-id="3d502-691">It is the inverse of the source map.</span></span>

<span data-ttu-id="3d502-692">El modelo empírico se usa directamente en el mapa de origen.</span><span class="sxs-lookup"><span data-stu-id="3d502-692">The empirical model is directly used in the source map.</span></span> <span data-ttu-id="3d502-693">En primer lugar, asigna los datos RGB especificados a los datos de CIELUV, que se convierten en datos XYZ.</span><span class="sxs-lookup"><span data-stu-id="3d502-693">It first maps a given RGB data into a CIELUV data, which is converted into XYZ data.</span></span> <span data-ttu-id="3d502-694">En el mapa de destino, los datos de CIEXYZ independientes del dispositivo se convierten primero en datos CIELUV.</span><span class="sxs-lookup"><span data-stu-id="3d502-694">In the destination map, device-independent CIEXYZ data is first converted into CIELUV data.</span></span> <span data-ttu-id="3d502-695">A continuación, se usan el modelo empírico y el método de Newton-Raphson clásico para predecir los mejores datos RGB para los datos de CIELUV.</span><span class="sxs-lookup"><span data-stu-id="3d502-695">Then, the empirical model and the classical Newton-Raphson method are used to predict the best RGB data for the CIELUV data.</span></span> <span data-ttu-id="3d502-696">Los detalles sobre la conversión de los datos de CieLUV a RGB son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3d502-696">The details about conversion from CieLUV to RGB data are as follows:</span></span>

<span data-ttu-id="3d502-697">Después de generar un LUT 3D de RGB a CieLUV, el mapa de RGB a LUV se crea con la interpolación tetrahedral en RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-697">After generating a 3-D LUT from RGB to CieLUV, the map from RGB to LUV is built using tetrahedral interpolation on RGB.</span></span> <span data-ttu-id="3d502-698">Este mapa se indica mediante las ecuaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="3d502-698">This map is denoted by the following equations:</span></span>

![Muestra las ecuaciones del mapa de R G B a L U V.](images/cdmp-image125.png)

<span data-ttu-id="3d502-700">La inversión de la asignación consiste en resolver, para cualquier color.</span><span class="sxs-lookup"><span data-stu-id="3d502-700">Inversion of the map consists of solving, for any color</span></span> ![Muestra L U V.](images/cdmp-image127.png) <span data-ttu-id="3d502-702">, el siguiente sistema de ecuaciones no lineales:</span><span class="sxs-lookup"><span data-stu-id="3d502-702">, the following system of nonlinear equations:</span></span>

![Muestra las ecuaciones no lineales para lolving cualquier color L U V.](images/cdmp-image129.png)

<span data-ttu-id="3d502-704">En la nueva CTE se usa una ecuación no lineal que se basa en el método de Newton-Raphson clásico.</span><span class="sxs-lookup"><span data-stu-id="3d502-704">A nonlinear equation that is based on the classical Newton-Raphson method is used in the new CTE.</span></span> <span data-ttu-id="3d502-705">Una estimación inicial o *una priori* See, s <sub>anteriores</sub> -(R 0, G 0, B 0) se obtiene al buscar en una "matriz de inicialización" que se compone de una cuadrícula de 8x8x8 uniforme de pares precalculados (RGB, Luv).</span><span class="sxs-lookup"><span data-stu-id="3d502-705">An initial guess, or *a priori* see, s <sub>prior</sub> -(R 0, G 0, B 0 ) is obtained by searching through a "seed matrix" consisting of a uniform 8x8x8 grid of pre-computed (RGB,Luv) pairs.</span></span> <span data-ttu-id="3d502-706">Se elige el Luv de RGB correspondiente más cercano a la L \* u \* v \* .</span><span class="sxs-lookup"><span data-stu-id="3d502-706">The RGB corresponding Luv that is closest to the L\*u\*v\* is chosen.</span></span> <span data-ttu-id="3d502-707">Cada punto de la matriz de inicialización corresponde al centro de una celda para que las iteraciones no empiecen por un punto en la superficie del límite del cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-707">Each point in the seed matrix corresponds to the center of a cell so that the iterations don't start with a point on the boundary face of the RGB cube.</span></span> <span data-ttu-id="3d502-708">En otras palabras, el RGB de las semillas se define mediante: paso = 1/8 s <sub>ijk</sub> = (paso/2 + (i-1) paso, paso/2 + (j-1) paso, paso/2 + (k-1) paso) con i, j, k = 1... 8 en el paso *i* de Newton-Raphson, la siguiente estimación ![ muestra las variables de la siguiente estimación.](images/cdmp-image133.png)</span><span class="sxs-lookup"><span data-stu-id="3d502-708">In other words, the RGB of the seeds is defined by: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) with i,j,k = 1...8 At the *i* th step of Newton-Raphson, the next estimate ![Shows the variables for the next estimate.](images/cdmp-image133.png)</span></span> <span data-ttu-id="3d502-709">se obtiene mediante la fórmula:</span><span class="sxs-lookup"><span data-stu-id="3d502-709">is obtained by the formula:</span></span>

![Muestra la fórmula para la estimación.](images/cdmp-image135.png)

<span data-ttu-id="3d502-711">La iteración se detiene cuando el error (distancia en el espacio CIELUV) es menor que un nivel de tolerancia preestablecido (0,1 en la CTE) o cuando el número de iteraciones ha superado el número máximo permitido de iteraciones (10 en la CTE).</span><span class="sxs-lookup"><span data-stu-id="3d502-711">Iteration stops when the error (distance in the CIELUV space) is less than a pre-set tolerance level (0.1 in the CTE), or when the number of iterations has exceeded the maximum allowed number of iterations (10 in the CTE).</span></span> <span data-ttu-id="3d502-712">Los valores de la tolerancia y el número de iteraciones se han determinado empíricamente como efectivos.</span><span class="sxs-lookup"><span data-stu-id="3d502-712">The values for the tolerance and the number of iterations were empirically determined to be effective.</span></span> <span data-ttu-id="3d502-713">En versiones futuras, se puede cambiar el valor de tolerancia.</span><span class="sxs-lookup"><span data-stu-id="3d502-713">In future versions, the tolerance value may be changed.</span></span>

<span data-ttu-id="3d502-714">La matriz Jacobian se calcula utilizando la diferencia hacia delante, excepto en un punto límite (una o varias de las R, G, B es 1) donde se usa la diferencia hacia atrás en su lugar.</span><span class="sxs-lookup"><span data-stu-id="3d502-714">The Jacobian matrix is calculated using forward difference, except at a boundary point (one or more of the R, G, B is 1) where backward difference is used instead.</span></span> <span data-ttu-id="3d502-715">En lugar de calcular el inverso de la matriz Jacobian, el sistema lineal se resuelve directamente utilizando Gauss-Jordan eliminación con dinamización completa.</span><span class="sxs-lookup"><span data-stu-id="3d502-715">Instead of calculating the inverse of the Jacobian matrix, the linear system is solved directly using Gauss-Jordan elimination with full pivoting.</span></span>

<span data-ttu-id="3d502-716">Al final de las iteraciones, es posible que no se logre la convergencia porque Newton-Raphson es un algoritmo "local", es decir, solo funciona bien si comienza con una estimación inicial cercana a la solución real.</span><span class="sxs-lookup"><span data-stu-id="3d502-716">At the end of the iterations, convergence still might not be achieved because Newton-Raphson is a "local" algorithm, that is, it only works well if you start with an initial guess that is close to the true solution.</span></span> <span data-ttu-id="3d502-717">Si, al final de la Newton-Raphson las iteraciones, no se ha logrado la convergencia dentro de la tolerancia a errores definida previamente, las iteraciones se reinician con un nuevo conjunto de inicializaciones, que se define de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="3d502-717">If, at the end of the Newton-Raphson iterations, convergence within the pre-defined error tolerance has not been achieved, the iterations are restarted with a new set of seeds, defined as follows.</span></span>

<span data-ttu-id="3d502-718">Por ejemplo, la mejor solución obtenida hasta ahora es (r, g, b).</span><span class="sxs-lookup"><span data-stu-id="3d502-718">For example, the best solution obtained so far is (r, g, b).</span></span> <span data-ttu-id="3d502-719">En esta solución, se derivan N inicializaciones posteriores, donde N = 4.</span><span class="sxs-lookup"><span data-stu-id="3d502-719">From this solution, N a posteriori seeds are derived, where N = 4.</span></span> <span data-ttu-id="3d502-720">Intuitivamente, la solución se mueve "hacia el centro" en un tamaño de paso que depende de N. Vea la figura 6.</span><span class="sxs-lookup"><span data-stu-id="3d502-720">Intuitively, the solution is moved "toward the center" in a step size that depends on N. See Figure 6.</span></span>

![Diagrama que muestra las direcciones Perturbation de la solución.](images/cdmp-image136.png)

<span data-ttu-id="3d502-722">**Figura 6** : la dirección Perturbation de la solución depende de la octeto en la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="3d502-722">**Figure 6** : Perturbation direction of the solution depends on which octant it is in.</span></span>

<span data-ttu-id="3d502-723">En otras palabras, si r &gt; 0,5, se reduce el valor del canal r; de lo contrario, se aumenta el valor.</span><span class="sxs-lookup"><span data-stu-id="3d502-723">In other words, if r &gt; 0.5, the value on the R channel is decreased, otherwise the value is increased.</span></span> <span data-ttu-id="3d502-724">Existe una lógica similar para los canales G y B.</span><span class="sxs-lookup"><span data-stu-id="3d502-724">There is similar logic for the G and B channels.</span></span> <span data-ttu-id="3d502-725">Las definiciones precisas son:</span><span class="sxs-lookup"><span data-stu-id="3d502-725">The precise definitions are:</span></span>

<span data-ttu-id="3d502-726">PERTURBATION = 0.5/(N + 1)</span><span class="sxs-lookup"><span data-stu-id="3d502-726">PERTURBATION = 0.5/(N+1)</span></span>

<span data-ttu-id="3d502-727">DIR (r) =-1 si r &gt; 0,5; + 1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d502-727">Dir(r) = -1 if r &gt; 0.5; +1 otherwise.</span></span> <span data-ttu-id="3d502-728">De forma similar para DIR (g) y DIR (b)</span><span class="sxs-lookup"><span data-stu-id="3d502-728">Similarly for Dir(g) and Dir(b)</span></span>

<span data-ttu-id="3d502-729">JTH a posteriori SEED, s????, es (r + DIR (r) \* j \* PERTURBATION, g + DIR (g) \* j \* PERTURBATION, b + DIR (b) \* j \* PERTURBATION)</span><span class="sxs-lookup"><span data-stu-id="3d502-729">The jth a posteriori seed, s ????, is (r + Dir(r) \*j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)</span></span>

<span data-ttu-id="3d502-730">Pruebe los primeros????</span><span class="sxs-lookup"><span data-stu-id="3d502-730">Try the first s ????</span></span> <span data-ttu-id="3d502-731">y si proporciona una nueva solución dentro de la tolerancia a errores, puede detenerse.</span><span class="sxs-lookup"><span data-stu-id="3d502-731">and if it gives a new solution within error tolerance, you can stop.</span></span> <span data-ttu-id="3d502-732">En caso contrario, pruebe los segundos????</span><span class="sxs-lookup"><span data-stu-id="3d502-732">Otherwise, try the second s ????</span></span> <span data-ttu-id="3d502-733">y así sucesivamente hasta el n????.</span><span class="sxs-lookup"><span data-stu-id="3d502-733">and so on until the Nth s ????.</span></span>

<span data-ttu-id="3d502-734">Los esquemas de todo el algoritmo se muestran en la figura 7.</span><span class="sxs-lookup"><span data-stu-id="3d502-734">The schematics of the whole algorithm is shown in Figure 7.</span></span>

![Diagrama que muestra el flujo para invertir el modelo de dispositivo.](images/cdmp-image138.png)

<span data-ttu-id="3d502-736">**Figura 7** : esquemas de invertir el modelo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d502-736">**Figure 7** : Schematics of inverting the device model</span></span>

### <a name="rgb-virtual-device-model-baseline"></a><span data-ttu-id="3d502-737">Línea base de modelo de dispositivo virtual RGB</span><span class="sxs-lookup"><span data-stu-id="3d502-737">RGB Virtual Device Model Baseline</span></span>

<span data-ttu-id="3d502-738">Este modelo de dispositivo (DM) es un algoritmo de reproducción de matriz/tono simple.</span><span class="sxs-lookup"><span data-stu-id="3d502-738">This device model(DM) is a simple matrix/tone reproduction algorithm.</span></span> <span data-ttu-id="3d502-739">La matriz se deriva del punto blanco y de los primarios mediante algoritmos de ciencia de color estándar.</span><span class="sxs-lookup"><span data-stu-id="3d502-739">The matrix is derived from the white point and primaries using standard color science algorithms.</span></span> <span data-ttu-id="3d502-740">La curva de reproducción de tono se deriva de los parámetros de medida según las descripciones de ICC de CurveType y ParametricType (o invertido según sea necesario).</span><span class="sxs-lookup"><span data-stu-id="3d502-740">The tone reproduction curve is derived from the measurement parameters according to the ICC descriptions of CurveType and ParametricType (or inverted as required).</span></span> <span data-ttu-id="3d502-741">Los detalles de los algoritmos internos se proporcionarán después de la validación adicional de problemas de intervalo dinámico elevados.</span><span class="sxs-lookup"><span data-stu-id="3d502-741">Details of the internal algorithms will be provided after additional validation of high dynamic range issues.</span></span>

<span data-ttu-id="3d502-742">El modelo de dispositivo virtual RGB es una curva de reproducción de matriz/tono ideal similar al diseño de perfil basado en la matriz de tres componentes de ICC.</span><span class="sxs-lookup"><span data-stu-id="3d502-742">The RGB virtual device model is an idealized matrix/tone reproduction curve RGB similar to the ICC three-component matrix-based profile design.</span></span> <span data-ttu-id="3d502-743">Los parámetros de "medida virtual" del DM incluyen un valor de punto blanco (CIEXYZ absoluto), valores principales de RGB (CIEXYZ absoluto) y una curva de reproducción de tono que se basa en la ParametricCurveType ICC y CurveType en formato XML coherente con los esquemas DMP.</span><span class="sxs-lookup"><span data-stu-id="3d502-743">The "virtual measurement" parameters of the DM include a white point value (absolute CIEXYZ), RGB primary values (absolute CIEXYZ), and a tone reproduction curve that is based on the ICC ParametricCurveType and CurveType in XML formatting consistent with the DMP schemas.</span></span>

<span data-ttu-id="3d502-744">En la tabla siguiente se muestran la codificación de tipo de función parametricCurveType de ICC y la compatibilidad correspondiente en IRGBVirtualDeviceModelBase.</span><span class="sxs-lookup"><span data-stu-id="3d502-744">ICC parametricCurveType function type encoding and corresponding support in IRGBVirtualDeviceModelBase are shown in the following table.</span></span>



| <span data-ttu-id="3d502-745">Tipo de función</span><span class="sxs-lookup"><span data-stu-id="3d502-745">Function type</span></span>                                         | <span data-ttu-id="3d502-746">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d502-746">Parameters</span></span>                          | <span data-ttu-id="3d502-747">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d502-747">Type</span></span>                                     | <span data-ttu-id="3d502-748">Nota:</span><span class="sxs-lookup"><span data-stu-id="3d502-748">Note</span></span>                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Muestra la función ' GammaType '.](images/cdmp-image154.png)<br/> | <span data-ttu-id="3d502-750">e</span><span class="sxs-lookup"><span data-stu-id="3d502-750">g</span></span><br/>              | <span data-ttu-id="3d502-751">GammaType</span><span class="sxs-lookup"><span data-stu-id="3d502-751">GammaType</span></span><br/>                 | <span data-ttu-id="3d502-752">Implementación común</span><span class="sxs-lookup"><span data-stu-id="3d502-752">Common implementation</span></span><br/>           |
| ![Muestra la función ' GammaOffsetGainType '.](images/cdmp-image156.png)<br/> | <span data-ttu-id="3d502-754">GA b</span><span class="sxs-lookup"><span data-stu-id="3d502-754">ga b</span></span><br/>           | <span data-ttu-id="3d502-755">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="3d502-755">GammaOffsetGainType</span></span><br/>       | <span data-ttu-id="3d502-756">CIE 122-1966</span><span class="sxs-lookup"><span data-stu-id="3d502-756">CIE 122-1966</span></span><br/>                    |
| ![Muestra la función ' GammaOffsetGainOffsetType '.](images/cdmp-image158.png)<br/> | <span data-ttu-id="3d502-758">GA b c</span><span class="sxs-lookup"><span data-stu-id="3d502-758">ga b c</span></span><br/>         | <span data-ttu-id="3d502-759">GammaOffsetGainOffsetType</span><span class="sxs-lookup"><span data-stu-id="3d502-759">GammaOffsetGainOffsetType</span></span><br/> | <span data-ttu-id="3d502-760">IEC 61966-3</span><span class="sxs-lookup"><span data-stu-id="3d502-760">IEC 61966-3</span></span><br/>                     |
| ![Muestra la función ' GammaOffsetGainGainType '.](images/cdmp-image160.png)<br/> | <span data-ttu-id="3d502-762">GA b c d</span><span class="sxs-lookup"><span data-stu-id="3d502-762">ga b c d</span></span><br/>       | <span data-ttu-id="3d502-763">GammaOffsetGainGainType</span><span class="sxs-lookup"><span data-stu-id="3d502-763">GammaOffsetGainGainType</span></span><br/>   | <span data-ttu-id="3d502-764">IEC 61966-2.1</span><span class="sxs-lookup"><span data-stu-id="3d502-764">IEC 61966-2.1</span></span><br/> <span data-ttu-id="3d502-765">sRGB</span><span class="sxs-lookup"><span data-stu-id="3d502-765">(sRGB)</span></span><br/> |
| ![Muestra una función para los parámetros ' g a b c d e f '.](images/cdmp-image162.png)<br/> | <span data-ttu-id="3d502-767">GA b c e f</span><span class="sxs-lookup"><span data-stu-id="3d502-767">ga b c d e f</span></span><br/>   | <span data-ttu-id="3d502-768">N/D</span><span class="sxs-lookup"><span data-stu-id="3d502-768">N/A</span></span><br/>                       | <span data-ttu-id="3d502-769">No se admite en WCS</span><span class="sxs-lookup"><span data-stu-id="3d502-769">Not supported in WCS</span></span><br/>            |



 

<span data-ttu-id="3d502-770">La curva de tono para dispositivos virtuales RGB se aplica en DeviceToColorimetric entre los datos de entrada, pDeviceColors y la multiplicación de la matriz.</span><span class="sxs-lookup"><span data-stu-id="3d502-770">The tone curve for RGB virtual devices is applied in DeviceToColorimetric between the input data, pDeviceColors, and the matrix multiply.</span></span> <span data-ttu-id="3d502-771">En el caso de ColorimetricToDevice, se debe usar un método para invertir la curva de tono.</span><span class="sxs-lookup"><span data-stu-id="3d502-771">For ColorimetricToDevice, a method must be used to invert the tone curve.</span></span> <span data-ttu-id="3d502-772">En la implementación de línea de base, esto se realiza mediante la interpolación directa en la misma curva de tono que se usa para DeviceToColorimetric.</span><span class="sxs-lookup"><span data-stu-id="3d502-772">In the baseline implementation, this is done by direct interpolation in the same tone curve used for DeviceToColorimetric.</span></span>

<span data-ttu-id="3d502-773">Las curvas se deben especificar en los perfiles como pares de números en el espacio float.</span><span class="sxs-lookup"><span data-stu-id="3d502-773">The curves should be specified in the profiles as pairs of numbers in float space.</span></span> <span data-ttu-id="3d502-774">El primer número representa los valores de pDeviceColors.</span><span class="sxs-lookup"><span data-stu-id="3d502-774">The first number represents values in pDeviceColors.</span></span> <span data-ttu-id="3d502-775">El segundo número representa la salida de la curva de tono.</span><span class="sxs-lookup"><span data-stu-id="3d502-775">The second number represents the output of the tone curve.</span></span> <span data-ttu-id="3d502-776">Todos los valores de la curva de tono deben estar entre minColorantUsed y maxColorantUsed.</span><span class="sxs-lookup"><span data-stu-id="3d502-776">All values in the tone curve must be between minColorantUsed and maxColorantUsed.</span></span> <span data-ttu-id="3d502-777">Las curvas de tono deben contener al menos dos entradas: una para minColorantUsed y otra para maxColorantUsed.</span><span class="sxs-lookup"><span data-stu-id="3d502-777">Tone curves must contain at least two entries: one for minColorantUsed and one for maxColorantUsed.</span></span> <span data-ttu-id="3d502-778">El número máximo de entradas en el ToneCurve es 2048.</span><span class="sxs-lookup"><span data-stu-id="3d502-778">The maximum number of entries in the ToneCurve is 2048.</span></span> <span data-ttu-id="3d502-779">En general, cuanto mayor sea el número de entradas de la tabla, más precisa podrá modelar la curvatura.</span><span class="sxs-lookup"><span data-stu-id="3d502-779">In general, the more entries in the table, the more accurately you can model curvature.</span></span> <span data-ttu-id="3d502-780">Se realiza una interpolación lineal a trozos entre las entradas.</span><span class="sxs-lookup"><span data-stu-id="3d502-780">A piecewise linear interpolation is performed between the entries.</span></span>

<span data-ttu-id="3d502-781">Puede considerar métodos de interpolación alternativos.</span><span class="sxs-lookup"><span data-stu-id="3d502-781">You might consider alternative interpolation methods.</span></span> <span data-ttu-id="3d502-782">Si sabe algo sobre el comportamiento subyacente del dispositivo, puede usar menos muestras y modelo con más precisión con una curva de orden superior.</span><span class="sxs-lookup"><span data-stu-id="3d502-782">If you know something about the underlying behavior of the device, you can use fewer samples and model more accurately with a higher order curve.</span></span> <span data-ttu-id="3d502-783">Pero si usa un tipo de curva incorrecto, será muy poco preciso.</span><span class="sxs-lookup"><span data-stu-id="3d502-783">But if you use the wrong curve type, you will be very inaccurate.</span></span> <span data-ttu-id="3d502-784">Sin más información, no puede adivinar el tipo de curva.</span><span class="sxs-lookup"><span data-stu-id="3d502-784">Without more information, you cannot guess the curve type.</span></span> <span data-ttu-id="3d502-785">Por lo tanto, use la interpolación lineal y proporcione muchos puntos de datos.</span><span class="sxs-lookup"><span data-stu-id="3d502-785">So, use linear interpolation and provide many data points.</span></span>

### <a name="cmyk-printer-device-model-baseline"></a><span data-ttu-id="3d502-786">Línea de base del modelo de dispositivo de impresora CMYK</span><span class="sxs-lookup"><span data-stu-id="3d502-786">CMYK Printer Device Model Baseline</span></span>

<span data-ttu-id="3d502-787">Una caracterización de dispositivos de una impresora CMYK consiste en construir un modelo empírico del dispositivo que predice el color impreso para cualquier valor CMYK determinado.</span><span class="sxs-lookup"><span data-stu-id="3d502-787">A device characterization of a CMYK printer consists of constructing an empirical model of the device that predicts the printed color for any given CMYK value.</span></span> <span data-ttu-id="3d502-788">La caracterización también incluye la inversion de este modelo para que se pueda imprimir una receta del valor CMYK para un color determinado.</span><span class="sxs-lookup"><span data-stu-id="3d502-788">The characterization also includes the inversion of this model so that a prescription of the CMYK value to us for a given color to be printed can be given.</span></span> <span data-ttu-id="3d502-789">Normalmente se define en términos de CIEXYZ o CIELAB.</span><span class="sxs-lookup"><span data-stu-id="3d502-789">This is typically defined in terms of CIEXYZ or CIELAB value.</span></span>

<span data-ttu-id="3d502-790">Normalmente, se utiliza un destino 8.7/3 que contiene revisiones CMYK.</span><span class="sxs-lookup"><span data-stu-id="3d502-790">Typically, an IT8.7/3 target containing CMYK patches is used.</span></span> <span data-ttu-id="3d502-791">Las revisiones consisten en el muestreo del espacio CMYK de una manera bien definida para que se forme una cuadrícula rectangular (con un espaciado no uniforme en C, M, y y K).</span><span class="sxs-lookup"><span data-stu-id="3d502-791">The patches consist of sampling of the CMYK space in a well-defined manner so that a rectangular grid (with non-uniform spacing in C, M, Y and K) is formed.</span></span> <span data-ttu-id="3d502-792">Después, cada revisión se mide con un colorimeter o un espectrofotómetro.</span><span class="sxs-lookup"><span data-stu-id="3d502-792">Each patch is then measured with a colorimeter or spectrophotometer.</span></span> <span data-ttu-id="3d502-793">Las medidas en los valores CIEXYZ forman una tabla de búsqueda (LUT), de la que se crea un modelo empírico de la impresora mediante el método de interpolación de Sakamoto.</span><span class="sxs-lookup"><span data-stu-id="3d502-793">The measurements in CIEXYZ values then form a lookup table (LUT), from which an empirical model of the printer is built using Sakamoto's interpolation method.</span></span> <span data-ttu-id="3d502-794">Patentes 4275413 de EE. UU. (Sakamoto et al.), patentes de EE. UU. 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="3d502-794">US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="3d502-795">Las dos patentes mencionadas han expirado.</span><span class="sxs-lookup"><span data-stu-id="3d502-795">The two patents mentioned have expired.</span></span>

<span data-ttu-id="3d502-796">Los requisitos específicos para los ejemplos de medida CMYK necesarios para que un perfil de modelo de dispositivo se acepte como válido por el modelo de dispositivo de línea de base de impresora CMYK son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="3d502-796">Specific requirements for the CMYK measurement samples necessary for a device model profile to be accepted as valid by the CMYK printer baseline device model are as follows.</span></span> <span data-ttu-id="3d502-797">(El conjunto de ejemplo se describe con mayor claridad como un conjunto de cubos de ejemplo CMY, cada uno asociado a un nivel K específico).</span><span class="sxs-lookup"><span data-stu-id="3d502-797">(The sample set is most clearly described as a set of CMY sample cubes, each associated with a specific K level.)</span></span>

-   <span data-ttu-id="3d502-798">Como mínimo, se deben proporcionar cubos CMY válidos para los niveles K = 0 y K = 100.</span><span class="sxs-lookup"><span data-stu-id="3d502-798">At minimum, valid CMY cubes must be provided for the K = 0 and K = 100 levels.</span></span>
-   <span data-ttu-id="3d502-799">Los niveles K intermedios pueden tener un espaciado no uniforme.</span><span class="sxs-lookup"><span data-stu-id="3d502-799">Intermediate K levels may be non-uniformly spaced.</span></span>
-   <span data-ttu-id="3d502-800">Se omitirá cualquier nivel K intermedio sin un cubo CMY válido.</span><span class="sxs-lookup"><span data-stu-id="3d502-800">Any intermediate K level without a valid CMY cube will be ignored.</span></span>
-   <span data-ttu-id="3d502-801">Los cubos CMY pueden utilizar intervalos de muestra no uniformes (espaciado de cuadrícula), pero el mismo conjunto de intervalos de muestra debe usarse en todas las dimensiones C, M e y del cubo CMY para un nivel K determinado.</span><span class="sxs-lookup"><span data-stu-id="3d502-801">The CMY cubes may use non-uniform sample intervals (grid spacing), but the same set of sample intervals must be used in all of the C,M, and Y dimensions in the CMY cube for a given K level.</span></span>
-   <span data-ttu-id="3d502-802">Cada cubo CMY de nivel K puede usar un número y espaciado diferentes de intervalos de muestra.</span><span class="sxs-lookup"><span data-stu-id="3d502-802">Each K level CMY cube can use a different number and spacing of sample intervals.</span></span>
-   <span data-ttu-id="3d502-803">Todos los cubos CMY deben contener las "esquinas" del cubo CMY, es decir, los ejemplos de CMY en \[ 0, 0, 0, \] \[ 0, 0100 \] , \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100.100 \] , \[ 100, 0100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .</span><span class="sxs-lookup"><span data-stu-id="3d502-803">All CMY cubes must contain the "corners" of the CMY cube, that is, CMY samples at \[0,0,0\], \[0,0,100\], \[0,100,0\], \[100,0,0\], \[0,100,100\], \[100,0,100\], \[100,100, 0\], \[100,100,100\].</span></span>
-   <span data-ttu-id="3d502-804">Cualquier nivel intermedio de la cuadrícula CMY debe ser totalmente muestreado en cada canal.</span><span class="sxs-lookup"><span data-stu-id="3d502-804">Any intermediate CMY grid levels must be fully sampled in each channel.</span></span> <span data-ttu-id="3d502-805">En otras palabras, debe existir un ejemplo en cada intersección de cuadrícula 3D dentro del cubo CMY.</span><span class="sxs-lookup"><span data-stu-id="3d502-805">In other words, a sample must exist at each 3-D grid intersection within the CMY cube.</span></span>
-   <span data-ttu-id="3d502-806">En el caso de los cubos K = 0 y K = 100 CMY, los cubos de 2x2x2 "solo esquinas" son los mínimos aceptados como válidos.</span><span class="sxs-lookup"><span data-stu-id="3d502-806">For the K = 0 and K = 100 CMY cubes, 2x2x2 "corners-only" cubes are the minimum accepted as valid.</span></span>

    <span data-ttu-id="3d502-807">\[Nota: para K = 0 y K = 100 niveles, se procesará un cubo de 3x3x3 CMY como un cubo 2x2x2 "Corners-Only". se omite el nivel de ejemplo intermedio.</span><span class="sxs-lookup"><span data-stu-id="3d502-807">\[NOTE: for K=0 and K=100 levels, a 3x3x3 CMY cube will be processed as a 2x2x2 "corners-only" cube; the intermediate sample level is ignored.</span></span> <span data-ttu-id="3d502-808">en los cubos de 4x4x4 y más grandes se utilizarán todos los ejemplos de la cuadrícula.\]</span><span class="sxs-lookup"><span data-stu-id="3d502-808">4x4x4 and larger cubes will have all on-grid samples used.\]</span></span>

-   <span data-ttu-id="3d502-809">En el caso de los niveles K intermedios, los cubos de 4x4x4 CMY son los mínimos aceptados como válidos.</span><span class="sxs-lookup"><span data-stu-id="3d502-809">For intermediate K levels, 4x4x4 CMY cubes are the minimum accepted as valid.</span></span>

<span data-ttu-id="3d502-810">Un perfil de alta calidad usará cuadrículas de muestreo más precisas que la mínima necesaria para la validez, normalmente 9x9x9x9 o superior.</span><span class="sxs-lookup"><span data-stu-id="3d502-810">A high-quality profile will use finer sampling grids than the minimum required for validity, usually 9x9x9x9 or higher.</span></span> <span data-ttu-id="3d502-811">Los ejemplos de los dispositivos de ti 8.7/3, IT 8.7/4 y ECI generan perfiles de modelo de dispositivo (DMPs) válidos para el modelo de dispositivo de línea de base de impresora CMYK.</span><span class="sxs-lookup"><span data-stu-id="3d502-811">The samples from the IT8.7/3, IT8.7/4, and ECI targets produce valid device model profiles (DMPs)for the CMYK printer baseline device model.</span></span> <span data-ttu-id="3d502-812">Aunque este modelo de dispositivo puede pasar por alto los ejemplos superfluos (fuera de la cuadrícula) en estos destinos, no se garantiza que pueda hacerlo para otros destinos y, por lo tanto, se recomienda que se quiten los ejemplos extraños de los conjuntos de medidas que entran en los perfiles de este modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d502-812">While this device model is able to ignore the extraneous (off-grid) samples in these targets, it is not guaranteed to be able to do so for other targets, and so, it is recommended that extraneous samples be removed from measurement sets going into profiles for this device model.</span></span>

<span data-ttu-id="3d502-813">La inversión del modelo de impresora presenta más dificultades.</span><span class="sxs-lookup"><span data-stu-id="3d502-813">The inversion of the printer model presents more difficulties.</span></span> <span data-ttu-id="3d502-814">Dado un color de entrada en CIECAM, hay una pregunta que indica si este color está dentro de la gama de la impresora.</span><span class="sxs-lookup"><span data-stu-id="3d502-814">Given an input color in CIECAM, there is a question of whether this color is within the printer gamut.</span></span> <span data-ttu-id="3d502-815">También hay un problema con respecto a la organización de puntos en el espacio de apariencia de color.</span><span class="sxs-lookup"><span data-stu-id="3d502-815">There is also the issue regarding the arrangement of points in the color appearance space.</span></span> <span data-ttu-id="3d502-816">Aunque podemos organizar los valores CMYK para que aparezcan en una cuadrícula rectangular, tal y como se hace en el destino 8.7/3, no se puede decir que los colores impresos resultantes se encuentran en el espacio de apariencia del color.</span><span class="sxs-lookup"><span data-stu-id="3d502-816">While we can arrange the CMYK values to fall on a rectangular grid, as is done in the IT8.7/3 target, the same cannot be said of the resulting printed colors as they are situated in the color appearance space.</span></span> <span data-ttu-id="3d502-817">En general, están dispersos en el espacio de apariencia de color sin un patrón determinado.</span><span class="sxs-lookup"><span data-stu-id="3d502-817">In general, they are scattered in the color appearance space with no particular pattern.</span></span>

<span data-ttu-id="3d502-818">Por lo general, hay dos enfoques para el problema de inversion de puntos dispersos.</span><span class="sxs-lookup"><span data-stu-id="3d502-818">There are generally two approaches to the inversion problem of scattered points.</span></span> <span data-ttu-id="3d502-819">Un enfoque consiste en usar una subdivisión geométrica de la gama de impresoras con sólidos de 3 dimensiones elementales, como tetrahedra.</span><span class="sxs-lookup"><span data-stu-id="3d502-819">One approach is to use a geometric subdivision of the printer gamut using elementary 3-dimensional solids, such as tetrahedra.</span></span> <span data-ttu-id="3d502-820">Una subdivisión de la gama de la impresora en el espacio de apariencia del color puede ser inducida por la Subdivisión correspondiente del espacio CMY (K), consulte bloqueo \[ 93 \] , Kang \[ 97 \] . Este enfoque tiene la ventaja de la simplicidad computacional.</span><span class="sxs-lookup"><span data-stu-id="3d502-820">A subdivision of the printer gamut in the color appearance space can be induced from the corresponding subdivision of the CMY(K) space, see Hung\[93\], Kang\[97\].This approach has the advantage of computational simplicity.</span></span> <span data-ttu-id="3d502-821">En el caso de Tetrahedron, solo se usan cuatro puntos en una interpolación.</span><span class="sxs-lookup"><span data-stu-id="3d502-821">In the case of a tetrahedron, only four points are used in an interpolation.</span></span> <span data-ttu-id="3d502-822">Por otro lado, el resultado depende en gran medida de unos cuantos puntos, lo que significa que un error de medición tendrá un efecto significativo en el resultado.</span><span class="sxs-lookup"><span data-stu-id="3d502-822">On the other hand, the result depends heavily on a few points, which means that a measurement error will have a significant effect on the result.</span></span> <span data-ttu-id="3d502-823">Interpolant también tiende a no ser tan suave.</span><span class="sxs-lookup"><span data-stu-id="3d502-823">The interpolant also tends to be not as smooth.</span></span> <span data-ttu-id="3d502-824">El segundo enfoque no supone ninguna subdivisión y se basa en la técnica de interpolación de datos diseminada.</span><span class="sxs-lookup"><span data-stu-id="3d502-824">The second approach does not assume any subdivision, and is based on the technique of scattered data interpolation.</span></span> <span data-ttu-id="3d502-825">Un ejemplo clásico es la técnica de la interpolación Charlene o el método ponderado inverso (consulte Charlene \[ 68 \] ).</span><span class="sxs-lookup"><span data-stu-id="3d502-825">A classical example is the technique of Shepard interpolation, or inverse weighted method (See Shepard \[68\]).</span></span> <span data-ttu-id="3d502-826">En este caso, se eligen varios puntos que rodean el punto de entrada de alguna manera, cada uno asignado a una ponderación, normalmente inversomente proporcional a la distancia, y el interpolant se toma como la media ponderada de los puntos vecinos.</span><span class="sxs-lookup"><span data-stu-id="3d502-826">Here, several points surrounding the input point are chosen in some manner, each assigned a weight, usually inversely proportional to the distance, and the interpolant is taken as the weighted average of the neighboring points.</span></span> <span data-ttu-id="3d502-827">En este enfoque, la elección de puntos contiguos es fundamental para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="3d502-827">In this approach, the choice of neighboring points is paramount to performance.</span></span> <span data-ttu-id="3d502-828">Aunque los pocos puntos pueden representar el interpolant inexacto y no Smooth, demasiados puntos imponen un elevado costo de cálculo, ya que las ponderaciones suelen ser funciones no lineales y costosas de calcular.</span><span class="sxs-lookup"><span data-stu-id="3d502-828">While too few points can render the interpolant inaccurate and non-smooth, too many points impose a high computational cost, as the weights are typically non-linear functions and costly to compute.</span></span>

<span data-ttu-id="3d502-829">Los dos enfoques descritos anteriormente tienen problemas.</span><span class="sxs-lookup"><span data-stu-id="3d502-829">The two approaches described above both have problems.</span></span> <span data-ttu-id="3d502-830">El enfoque de subdivisión depende de los datos que sean razonablemente nulos de ruido y, por lo general, el interpolant no es muy suave.</span><span class="sxs-lookup"><span data-stu-id="3d502-830">The subdivision approach depends critically on the data being reasonably void of noise, and generally the interpolant is not very smooth.</span></span> <span data-ttu-id="3d502-831">La interpolación de datos diseminada es más tolerante al ruido de los datos y, por lo general, proporciona un interpolant más suave, pero es computacionalmente más caro.</span><span class="sxs-lookup"><span data-stu-id="3d502-831">The scattered data interpolation is more tolerant to data noise, and generally gives a smoother interpolant, but it is computationally more expensive.</span></span>

<span data-ttu-id="3d502-832">La nueva CTE toma un enfoque alternativo.</span><span class="sxs-lookup"><span data-stu-id="3d502-832">The new CTE takes an alternative approach.</span></span> <span data-ttu-id="3d502-833">El dispositivo CMYK se trata como una colección de varios dispositivos CMY, cada uno de los cuales tiene un valor específico de negro (K).</span><span class="sxs-lookup"><span data-stu-id="3d502-833">The CMYK device is treated as a collection of several CMY devices, each of which has a specific value of black (K).</span></span> <span data-ttu-id="3d502-834">El uso de un algoritmo de selección que toma como luz y intensidad de los parámetros se elige un nivel de negro.</span><span class="sxs-lookup"><span data-stu-id="3d502-834">Using a selection algorithm that takes as parameters lightness and chroma, a level of black is chosen.</span></span> <span data-ttu-id="3d502-835">Los valores CMY se obtienen mediante la inversion de la tabla de CMY a Luv correspondiente con los métodos de Newton utilizados en otra parte por el algoritmo de impresora RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-835">The CMY values are obtained by inversion of the corresponding CMY to Luv table using the Newton methods employed elsewhere by the RGB printer algorithm.</span></span>

<span data-ttu-id="3d502-836">Siga los pasos que se describen a continuación.</span><span class="sxs-lookup"><span data-stu-id="3d502-836">Use the following steps.</span></span>

1.  <span data-ttu-id="3d502-837">Imprime el destino de la caracterización, que es el destino 8.7/3, o un destino que contiene el muestreo del espacio CMYK con intervalos de espaciado frecuente o irregular.</span><span class="sxs-lookup"><span data-stu-id="3d502-837">Print the characterization target, which is either the IT8.7/3 target, or a target containing sampling of the CMYK space at regularly or irregularly spaced intervals.</span></span>
2.  <span data-ttu-id="3d502-838">Mida el destino mediante un espectrofotómetro y convierta las medidas en el espacio de CIELUV.</span><span class="sxs-lookup"><span data-stu-id="3d502-838">Measure the target using a spectrophotometer, and convert the measurements to CIELUV space.</span></span>
3.  <span data-ttu-id="3d502-839">Construya el mapa hacia delante de CMYK a Luv.</span><span class="sxs-lookup"><span data-stu-id="3d502-839">Construct the forward map from CMYK to Luv.</span></span>
4.  <span data-ttu-id="3d502-840">Use el mapa de avance para construir un conjunto de Luv para un intervalo de valores K.</span><span class="sxs-lookup"><span data-stu-id="3d502-840">Use the forward map to construct a set of CMY to Luv maps for a range of K values.</span></span>
5.  <span data-ttu-id="3d502-841">Para cualquier valor de Luv de entrada, el valor CMYK correspondiente se obtiene seleccionando uno de los mapas construidos en el paso 4 anterior e invirtiendo con el método de Newton para obtener un conjunto de Colorant CMY que acompañe al valor K seleccionado.</span><span class="sxs-lookup"><span data-stu-id="3d502-841">For any input Luv value, the corresponding CMYK value is obtained by selecting one of the maps constructed in step 4 above and inverting using Newton's method to obtain a CMY colorant set to accompany the K value selected.</span></span>

<span data-ttu-id="3d502-842">Los pasos 1 y 2, que son procedimientos estándar, los realiza un programa de generación de perfiles que no forma parte de la nueva CTE.</span><span class="sxs-lookup"><span data-stu-id="3d502-842">Steps 1 and 2, which are standard procedures, are performed by a profiling program that is not part of the new CTE.</span></span> <span data-ttu-id="3d502-843">El destino 8.7/3 contiene un muestreo razonablemente detallado de todos los valores CMYK en distintos niveles de C, M, y y K. como alternativa, se puede usar un destino personalizado con un muestreo uniforme de los canales C, M, y y K.</span><span class="sxs-lookup"><span data-stu-id="3d502-843">The IT8.7/3 target contains a reasonably detailed sampling of all the CMYK values at various levels of C, M, Y, and K. Alternatively, a custom target with uniform sampling of the C, M, Y, and K channels can be used.</span></span> <span data-ttu-id="3d502-844">Una vez que se imprime el destino, se puede usar un espectrofotómetro o colorimeter para medir el valor XYZ de cada revisión y el valor XYZ se puede convertir al valor Luv mediante el modelo CIELUV.</span><span class="sxs-lookup"><span data-stu-id="3d502-844">After the target is printed, a spectrophotometer or colorimeter can be used to measure the XYZ value of each patch, and the XYZ value can be converted to the Luv value using the CIELUV model.</span></span>

<span data-ttu-id="3d502-845">El paso 3, la construcción del mapa hacia delante de CMYK a Luv, se puede lograr aplicando cualquier técnica de interpolación conocida, como un método multilineal o tetrahedral, en la cuadrícula rectangular en el espacio CMYK.</span><span class="sxs-lookup"><span data-stu-id="3d502-845">Step 3, construction of the forward map from CMYK to Luv, can be achieved by applying any known interpolation technique, such as tetrahedral or multilinear method, on the rectangular grid in CMYK space.</span></span> <span data-ttu-id="3d502-846">En la nueva CTE, se usa una interpolación tetrahedral de 4 dimensiones.</span><span class="sxs-lookup"><span data-stu-id="3d502-846">In the new CTE, a 4-dimensional tetrahedral interpolation is used.</span></span> <span data-ttu-id="3d502-847">Dado que las cuadrículas de muestreo de CMY suelen ser diferentes en cada nivel de K, sin embargo, usamos una técnica de supermuestreo, tal y como se detalla a continuación.</span><span class="sxs-lookup"><span data-stu-id="3d502-847">Because the CMY sampling grids are generally different on each level of K, however, we use a technique of super-sampling, as detailed below.</span></span> <span data-ttu-id="3d502-848">En el caso de un punto CMYK determinado, los niveles de la sandwich se determinan en primer lugar en función del valor K.</span><span class="sxs-lookup"><span data-stu-id="3d502-848">For a given CMYK point, the sandwiching K levels are first determined based on the K value.</span></span> <span data-ttu-id="3d502-849">A continuación, introduzca una "supercuadrícula" en cada nivel K que sea una Unión de las cuadrículas de CMY en cada uno de los dos niveles de K.</span><span class="sxs-lookup"><span data-stu-id="3d502-849">Then introduce a "super-grid" on each K level that is a union of the CMY grids on each of the two K levels.</span></span> <span data-ttu-id="3d502-850">En cada nivel K, el valor Luv de cualquier punto de cuadrícula recién introducido se obtiene mediante una interpolación tetrahedral tridimensional dentro de ese nivel K.</span><span class="sxs-lookup"><span data-stu-id="3d502-850">On each K level, the Luv value of any newly introduced grid point is obtained by a 3-dimensional tetrahedral interpolation within that K level.</span></span> <span data-ttu-id="3d502-851">Por último, en esta nueva cuadrícula se realiza una interpolación tetrahedral de 4 dimensiones para el punto CMYK específico.</span><span class="sxs-lookup"><span data-stu-id="3d502-851">Finally, a 4-dimensional tetrahedral interpolation for the specific CMYK point is performed on this new grid.</span></span>

![Diagrama que muestra el supermuestreo.](images/cdmp-image163.png)

<span data-ttu-id="3d502-853">**Figura 8** : supermuestreo</span><span class="sxs-lookup"><span data-stu-id="3d502-853">**Figure 8** : Supersampling</span></span>

<span data-ttu-id="3d502-854">El paso 4 crea un conjunto de tablas de búsqueda de CMY a Luv (LUTs).</span><span class="sxs-lookup"><span data-stu-id="3d502-854">Step 4 constructs a set of CMY-to-Luv lookup tables (LUTs).</span></span> <span data-ttu-id="3d502-855">El mapa hacia delante construido en el paso 3 se llama repetidamente para volver a muestrear el espacio CMYK.</span><span class="sxs-lookup"><span data-stu-id="3d502-855">The forward map constructed in Step 3 is called repeatedly to resample the CMYK space.</span></span> <span data-ttu-id="3d502-856">El espacio de colores CMYK se muestrea con un espaciado uniforme de K y otro, pero sigue uniformemente espaciado, muestreo de CMY.</span><span class="sxs-lookup"><span data-stu-id="3d502-856">The CMYK color space is sampled using an even spacing of K and a different, but still evenly spaced, sampling of CMY.</span></span>

<span data-ttu-id="3d502-857">El paso 5 es un procedimiento para obtener el valor CMYK mediante el LUTs construido en el paso 4 para cualquier punto de Luv de entrada.</span><span class="sxs-lookup"><span data-stu-id="3d502-857">Step 5 is a procedure to obtain the CMYK value using the LUTs constructed in Step 4 for any input Luv point.</span></span> <span data-ttu-id="3d502-858">El valor adecuado de K se elige mediante el análisis de la luminosidad y el grado de color de la Luv solicitada.</span><span class="sxs-lookup"><span data-stu-id="3d502-858">The appropriate value of K is chosen by analyzing the lightness as well as the degree of color in the Luv requested.</span></span> <span data-ttu-id="3d502-859">Una vez seleccionada la tabla, los valores CMY se obtienen de la tabla mediante el método de Newton (como se documenta en el modelo de dispositivo de impresora RGB anterior).</span><span class="sxs-lookup"><span data-stu-id="3d502-859">After the table is selected, the CMY values are obtained from the table by using Newton's method (as documented under the RGB printer device model earlier).</span></span>

<span data-ttu-id="3d502-860">El espacio CIELUV se usa en el modelo de impresora en lugar de CIEJab porque el modelo de dispositivo debe estar basado únicamente en los datos de colorimétrico disponibles en el DMP.</span><span class="sxs-lookup"><span data-stu-id="3d502-860">CIELUV space is used in the printer model instead of CIEJab because the device model should be based solely on colorimetric data available in the DMP.</span></span> <span data-ttu-id="3d502-861">El DMP contiene datos colorimétrico para cada revisión medida, incluido el punto blanco multimedia, por lo que es posible convertir los datos de CIEXYZ en datos de CIELUV.</span><span class="sxs-lookup"><span data-stu-id="3d502-861">The DMP contains colorimetric data for each measured patch, including the media white point, so it is possible to convert CIEXYZ data into CIELUV data.</span></span> <span data-ttu-id="3d502-862">Sin embargo, no es posible convertir a CIECAM02 JCh o jab, ya que no hay acceso a la información de la condición de visualización en el DMP.</span><span class="sxs-lookup"><span data-stu-id="3d502-862">However, it is not possible to convert to CIECAM02 JCh or Jab, because there is no access to the viewing condition information in the DMP.</span></span>

### <a name="rgb-projector-device-model-baseline"></a><span data-ttu-id="3d502-863">Línea de base del modelo de dispositivo de proyector RGB</span><span class="sxs-lookup"><span data-stu-id="3d502-863">RGB Projector Device Model Baseline</span></span>

<span data-ttu-id="3d502-864">Nota: muchos proyectores de RGB tienen más de un modo de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="3d502-864">Note: Many RGB projectors have more than one operating mode.</span></span> <span data-ttu-id="3d502-865">En un modo, que suele ser el valor predeterminado y se puede llamar algo parecido a "presentación", la respuesta de color del proyector está optimizada para obtener el máximo brillo.</span><span class="sxs-lookup"><span data-stu-id="3d502-865">In one mode, which is often the default and might be called something like "presentation," the color response of the projector is optimized for maximum brightness.</span></span> <span data-ttu-id="3d502-866">Sin embargo, en este modo, el proyector pierde la capacidad de reproducir colores claros, ligeramente cromáticos, como amarillos pálidos y algunos tonos de piel.</span><span class="sxs-lookup"><span data-stu-id="3d502-866">However, in this mode, the projector loses the ability to reproduce light, slightly chromatic colors such as pale yellows and some flesh tones.</span></span> <span data-ttu-id="3d502-867">En otro modo, a menudo denominado "película", "vídeo" o "sRGB", el proyector está optimizado para la reproducción de imágenes realistas y escenas naturales.</span><span class="sxs-lookup"><span data-stu-id="3d502-867">In another mode, often called "film," "video," or "sRGB," the projector is optimized for reproduction of realistic images and natural scenes.</span></span> <span data-ttu-id="3d502-868">En este modo, el brillo máximo se renegocia para mejorar la calidad general de la reproducción de color.</span><span class="sxs-lookup"><span data-stu-id="3d502-868">In this mode, maximum brightness is traded off to improve the overall quality of the color reproduction.</span></span> <span data-ttu-id="3d502-869">Para obtener una reproducción de color satisfactoria con proyectores RGB, es necesario colocar el proyector en un modo en el que se pueda reproducir una gama de colores fluida.</span><span class="sxs-lookup"><span data-stu-id="3d502-869">To obtain satisfactory color reproduction with RGB projectors, it is necessary to place the projector in a mode where a smooth gamut of colors can be reproduced.</span></span>

![Diagrama que muestra un modelo de dispositivo D L P.](images/cdmp-image167.png)

<span data-ttu-id="3d502-871">**Figura 9** : modelo de dispositivo DLP</span><span class="sxs-lookup"><span data-stu-id="3d502-871">**Figure 9** : DLP device model</span></span>

<span data-ttu-id="3d502-872">Un valor RGB entrante pasa por dos rutas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="3d502-872">An incoming RGB value passes through two computational pathways.</span></span> <span data-ttu-id="3d502-873">El primero es el modelo de matriz, que da como resultado un valor XYZ.</span><span class="sxs-lookup"><span data-stu-id="3d502-873">The first is the matrix model, which results in an XYZ value.</span></span> <span data-ttu-id="3d502-874">Esto va seguido inmediatamente de la conversión de XYZ a Luv.</span><span class="sxs-lookup"><span data-stu-id="3d502-874">This is immediately followed by the conversion from XYZ to Luv.</span></span> <span data-ttu-id="3d502-875">La segunda es la interpolación LUT no uniforme mediante la interpolación tetrahedral.</span><span class="sxs-lookup"><span data-stu-id="3d502-875">The second is the non-uniform LUT interpolation using tetrahedral interpolation.</span></span> <span data-ttu-id="3d502-876">La salida de la interpolación ya está en el espacio Luv por construcción.</span><span class="sxs-lookup"><span data-stu-id="3d502-876">The output of the interpolation is already in Luv space by construction.</span></span> <span data-ttu-id="3d502-877">Las dos salidas se agregan para obtener el valor de Luv predicho.</span><span class="sxs-lookup"><span data-stu-id="3d502-877">The two outputs are added to obtain the predicted Luv value.</span></span> <span data-ttu-id="3d502-878">Finalmente, esto se convierte en XYZ, que es la salida esperada del modelo de colorimétrica para el dispositivo DLP.</span><span class="sxs-lookup"><span data-stu-id="3d502-878">This is finally converted to XYZ, which is the expected output of the colorimetric model for the DLP device.</span></span>

<span data-ttu-id="3d502-879">Dado que los proyectores son dispositivos de pantalla, también admiten la inversion del modelo, es decir, la transformación de XYZ a RGB.</span><span class="sxs-lookup"><span data-stu-id="3d502-879">Since projectors are display devices, they also support the inversion of the model, that is, the transform from XYZ to RGB.</span></span> <span data-ttu-id="3d502-880">Dado que el modelo de dispositivo transforma el espacio RGB en espacio XYZ, que son ambos de tres dimensiones, la inversión es equivalente a la resolución de tres ecuaciones no lineales en tres desconocidos.</span><span class="sxs-lookup"><span data-stu-id="3d502-880">Because the device model transforms RGB space to XYZ space, which are both three dimensional, inversion is equivalent to solving three nonlinear equations in three unknowns.</span></span> <span data-ttu-id="3d502-881">Esto puede realizarse mediante técnicas de resolución de ecuaciones estándar, como Newton-Raphson.</span><span class="sxs-lookup"><span data-stu-id="3d502-881">This can done by standard equation solving techniques, such as Newton-Raphson.</span></span> <span data-ttu-id="3d502-882">Sin embargo, es preferible convertir primero XYZ en Luv y, a continuación, invertir el Luv en transformación RGB, ya que el espacio Luv es más linealmente lineal que el espacio XYZ.</span><span class="sxs-lookup"><span data-stu-id="3d502-882">It is preferable, however, to first convert XYZ to Luv, and then invert the Luv To RGB transform, because Luv space is more perceptually linear than XYZ space.</span></span>

### <a name="icc-device-model-baseline"></a><span data-ttu-id="3d502-883">Línea de base del modelo de dispositivo ICC</span><span class="sxs-lookup"><span data-stu-id="3d502-883">ICC Device Model Baseline</span></span>

<span data-ttu-id="3d502-884">La interoperabilidad de los flujos de trabajo de ICC CITAda se habilita mediante la creación de un perfil de modelo de dispositivo de línea de base de dispositivo ICC especial que almacena el objeto de perfil y crea una transformación ICC mediante un perfil de empresa no operativa.</span><span class="sxs-lookup"><span data-stu-id="3d502-884">The CITE ICC workflow interoperability is enabled by creating a special ICC device baseline device model profile that stores the profile object and creates a ICC transform using a no-op XYZ profile.</span></span> <span data-ttu-id="3d502-885">Esta transformación se usa para la conversión entre los colores de dispositivo y CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="3d502-885">This transform is then used to translate between device and CIEXYZ colors.</span></span>

![Diagrama que muestra la interoperabilidad de flujo de trabajo c I T E I c i.](images/cdmp-image168.png)

<span data-ttu-id="3d502-887">**Figura 10** : interoperabilidad de los flujos de trabajo de ICC</span><span class="sxs-lookup"><span data-stu-id="3d502-887">**Figure 10** : CITE ICC Workflow Interoperability</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d502-888">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d502-888">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d502-889">Conceptos básicos de la administración del color</span><span class="sxs-lookup"><span data-stu-id="3d502-889">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="3d502-890">Algoritmos y esquemas del Sistema de colores de Windows</span><span class="sxs-lookup"><span data-stu-id="3d502-890">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





