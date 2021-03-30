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
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>Algoritmos y esquema de perfil del modelo de dispositivo de color de WCS

En este tema se proporciona información sobre el esquema de Perfil de modelo de dispositivo de color WCS y sus algoritmos asociados.

Este tema contiene las siguientes secciones:

-   [Información general](#overview)
-   [Arquitectura de Perfil de modelo de dispositivo de color](#color-device-model-profile-architecture)
-   [El esquema CDMP](#the-cdmp-schema)
-   [Adición de calibración de CDMP v 2.0 de WCS](#wcs-cdmp-v20-calibration-addition)
-   [Los elementos de esquema CDMP](#the-cdmp-schema-elements)
    -   [ColorDeviceModelProfile](#colordevicemodelprofile)
    -   [ColorDeviceModel](#colordevicemodelprofile)
    -   [NamespaceVersion](#namespaceversion)
    -   [Versión](#namespaceversion)
    -   [Documentación](#documentation)
    -   [Elemento CRTDevice](#crtdevice-element)
    -   [Elemento LCDDevice](#lcddevice-element)
    -   [Elemento ProjectorDevice](#projectordevice-element)
    -   [Elemento ScannerDevice](#scannerdevice-element)
    -   [Elemento CameraDevice](#cameradevice-element)
    -   [Elemento RGBPrinterDevice](#rgbprinterdevice-element)
    -   [Elemento CMYKPrinterDevice](#cmykprinterdevice-element)
    -   [Elemento RGBVirtualDevice](#rgbvirtualdevice-element)
    -   [PlugInDeviceType](#plugindevicetype)
    -   [RGBVirtualMeasurementType](#rgbvirtualmeasurementtype)
    -   [GammaType](#gammatype)
    -   [GammaOffsetGainType](#gammaoffsetgaintype)
    -   [GammaOffsetGainLinearGainType](#gammaoffsetgainlineargaintype)
    -   [ToneResponseCurvesType](#toneresponsecurvestype)
    -   [GamutBoundarySamplesType](#gamutboundarysamplestype)
    -   [FloatPairList](#floatpairlist)
    -   [CMYKPrinterMeasurementType](#cmykprintermeasurementtype)
    -   [RGBPrinterMeasurementType](#rgbprintermeasurementtype)
    -   [RGBCaptureMeasurementType](#rgbcapturemeasurementtype)
    -   [OneBasedIndex](#onebasedindex)
    -   [RGBProjectorMeasurementType](#rgbprojectormeasurementtype)
    -   [DisplayMeasurementType](#displaymeasurementtype)
    -   [MeasurementConditionsType](#measurementconditionstype)
    -   [GeometryType](#geometrytype)
    -   [RGBPrimariesGroup](#rgbprimariesgroup)
    -   [NonNegativeCMYKSampleType](#nonnegativecmyksampletype)
    -   [NonNegativeRGBSampleType](#nonnegativergbsampletype)
    -   [NonNegativeCMYKType](#nonnegativecmyktype)
    -   [NonNegativeRGBType](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [NonNegativeXYZType](#nonnegativexyztype)
    -   [XYZType](#nonnegativexyztype)
-   [Algoritmos de línea de base de CDMP](#the-cdmp-baseline-algorithms)
    -   [Línea de base del modelo de dispositivo CRT](#crt-device-model-baseline)
    -   [Línea de base del modelo de dispositivo LCD](#lcd-device-model-baseline)
    -   [Línea base del modelo de dispositivo de impresora RGB](#rgb-printer-device-model-baseline)
    -   [Línea base de modelo de dispositivo virtual RGB](#rgb-virtual-device-model-baseline)
    -   [Línea de base del modelo de dispositivo de impresora CMYK](#cmyk-printer-device-model-baseline)
    -   [Línea de base del modelo de dispositivo de proyector RGB](#rgb-projector-device-model-baseline)
    -   [Línea de base del modelo de dispositivo ICC](#icc-device-model-baseline)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Este esquema se utiliza para especificar el contenido de un perfil de modelo de dispositivo de color (CDMP). A continuación se describen los algoritmos de línea de base asociados.

El esquema de Perfil de modelo de dispositivo básico (DMP) consta de los datos de medición de muestreo.

El componente de muestreo del esquema XML de DMP proporciona compatibilidad con los objetivos básicos de medición de color, centrándose en los destinos estándar comunes y los destinos optimizados para los modelos de dispositivo de línea de base.

Además, el perfil de dispositivo proporciona información específica sobre el modelo de dispositivo de destino y proporciona una directiva que el modelo de dispositivo de reserva de línea de base puede usar si el modelo de destino no está disponible. Las instancias de perfil pueden incluir extensiones privadas mediante mecanismos de extensión XML estándar.

## <a name="color-device-model-profile-architecture"></a>Arquitectura de Perfil de modelo de dispositivo de color

![Diagrama que muestra la información que constituye un perfil de modelo de dispositivo.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>El esquema CDMP


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



## <a name="wcs-cdmp-v20-calibration-addition"></a>Adición de calibración de CDMP v 2.0 de WCS

El elemento **ColorDeviceModel** del esquema CDMP se ha actualizado en Windows 7 para incluir el nuevo elemento de calibración. A continuación se muestra el cambio en el esquema CDMP.


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



## <a name="the-cdmp-schema-elements"></a>Los elementos de esquema CDMP

> [!Note]  
> Los primarios son muestras principales de rojo, verde, azul, negro y blanco. Una rampa principal es una rampa tonal de menos luminancia hasta el valor principal completo. El número máximo de entradas en una rampa de tono es 4096.

 

> [!Note]  
> DMPs son necesarios para tener datos de medición.

 

### <a name="colordevicemodelprofile"></a>ColorDeviceModelProfile

Este elemento es de tipo ColorDeviceModel.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="colordevicemodel"></a>ColorDeviceModel

Este elemento es una secuencia de los siguientes subelementos

1.  Cadena de perfilename,
2.  cadena de descripción opcional,
3.  cadena de autor opcional,
4.  opcional MeasurementConditions MeasurementConditionsType,
5.  Self-Luminous Boolean,
6.  MaxColorant Float,
7.  MinColorant Float,
8.  Elección de los elementos
    1.  CRTDevice,
    2.  LCDDevice,
    3.  RGBProjectorDevice,
    4.  ScannerDevice,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  CMYKPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. Extensión opcional ExtensionType

**Condiciones de validación:** Cada subelemento se valida por su propio tipo. Los subelementos de cadena tienen un máximo de 10.000 caracteres. El subelemento MaxColorant debe ser mayor o igual que cero (0) y mayor que el subelemento MinColorant. El valor de MinColorant puede ser negativo.

### <a name="namespaceversion"></a>NamespaceVersion

xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Versión

Versión = "1,0" con Windows Vista.

**Condiciones de validación:** Cualquier valor de versión &gt; 0,1 o &lt; = 2,0 es válido para admitir cambios no importantes en el formato.

### <a name="documentation"></a>Documentación

Esquema de Perfil de modelo de dispositivo.

Copyright (C) Microsoft. Todos los derechos reservados.

### <a name="crtdevice-element"></a>Elemento CRTDevice

Este elemento es una secuencia de subelementos de un MeasurementData DisplayMeasurementType.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="lcddevice-element"></a>Elemento LCDDevice

Este elemento es una secuencia de subelementos de un MeasurementData DisplayMeasurementType.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="projectordevice-element"></a>Elemento ProjectorDevice

Este elemento es una secuencia de subelementos de un MeasurementData RGBProjectorMeasurementType.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="scannerdevice-element"></a>Elemento ScannerDevice

Este elemento es una secuencia de subelementos de un MeasurementData RGBCaptureMeasurementType

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="cameradevice-element"></a>Elemento CameraDevice

Este elemento es una secuencia de subelementos de un MeasurementData RGBCaptureMeasurementType

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="rgbprinterdevice-element"></a>Elemento RGBPrinterDevice

Este elemento es una secuencia de subelementos de un MeasurementData RGBPrinterMeasurementType.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="cmykprinterdevice-element"></a>Elemento CMYKPrinterDevice

Este elemento es una secuencia de subelementos de un MeasurementData CMYKPrinterMeasurementType.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="rgbvirtualdevice-element"></a>Elemento RGBVirtualDevice

Este elemento es una secuencia de subelementos de un RGBVirtualMeasurementDataType.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

### <a name="plugindevicetype"></a>PlugInDeviceType

Este elemento es una secuencia de un GUIDType de GUID y cualquier subelemento.

**Condiciones de validación:** El GUID se usa para hacer coincidir el GUID del archivo DLL del complemento DM. Hay un máximo de 100.000 subelementos personalizados.

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

Este elemento es una secuencia que consta de

1.  Grupo RGBPrimariesGroup
2.  Una opción de
3.  -   Gamma
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   Elementos ToneResponseCurves

4.  GamutBoundarySamples GamutBoundarySamplesType opcional
5.  TimeStamp dateTime

**Condiciones de validación:** Cada subelemento de estos tipos tiene sus propias condiciones de validación.

### <a name="gammatype"></a>GammaType

Este elemento es un tipo complejo que se compone del atributo

-   NonNegativeFloatType gamma

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

Este elemento es un tipo complejo que consta de los atributos

-   NonNegativeFloatType gamma
-   Desplazamiento NonNegativeFloatType
-   Obtener NonNegativeFloatType

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

Este elemento es un tipo complejo que consta de los atributos

-   NonNegativeFloatType gamma
-   Desplazamiento NonNegativeFloatType
-   Obtener NonNegativeFloatType
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

Este elemento es una secuencia de

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

El elemento también tiene un atributo TRCLength de tipo unsignedint.

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

Este elemento es una secuencia de RGBTypes RGB.

**Condiciones de validación:** Repeticiones máximas sin enlazar actualmente, que se van a restringir en función de los comentarios del sector.

### <a name="floatpairlist"></a>FloatPairList

Este elemento es un tipo simple de lista de pares de elementos flotantes.

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="cmykprintermeasurementtype"></a>CMYKPrinterMeasurementType

Este elemento es un

1. secuencia del elemento ColorCube que consta de una secuencia de NonNegativeCMYKSampleType de ejemplo

2. Atributo TimeStamp dateTime.

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

Este elemento es un

1. secuencia del elemento ColorCube que consta de una secuencia de NonNegativeRGBSampleType de ejemplo

2. Atributo TimeStamp dateTime.

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

Este elemento es una secuencia de

1.  PrimaryIndex complexType de
2.  1.  OneBasedIndex blanco
    2.  OneBasedIndex negro opcional
    3.  OneBasedIndex rojo opcional
    4.  OneBasedIndex verde opcional
    5.  OneBasedIndex azul opcional
    6.  OneBasedIndex cian opcional
    7.  OneBasedIndex magenta opcional
    8.  OneBasedIndex amarillo opcional

3.  NeutralIndices de líneas de OneBasedIndex
4.  ColorSamples secuencia de NonNegativeRGBSampleType de ejemplo

El elemento también tiene un atributo TimeStamp dateTime.

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="onebasedindex"></a>OneBasedIndex

Este elemento es un tipo simple del int sin signo de base de restricción con valor de minInclusive = "1".

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

Este elemento es una secuencia de

1.  Grupo RGBPrimariesGroup
2.  elemento ColorSamples que consta de una secuencia de NonNegativeRGBSampleType de ejemplo

El elemento también tiene un atributo TimeStamp dateTime.

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

Este elemento es una secuencia de

1.  Grupo RGBPrimariesGroup
2.  GrayRamp de la secuencia de NonNegativeRGBType de ejemplo
3.  RedRamp de la secuencia de NonNegativeRGBType de ejemplo
4.  GreenRamp de la secuencia de NonNegativeRGBType de ejemplo
5.  BlueRamp de la secuencia de NonNegativeRGBType de ejemplo

El elemento DisplayMeasurementType también tiene un atributo TimeStamp dateTime.

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="measurementconditionstype"></a>MeasurementConditionsType

MeasurementConditionsType es una secuencia de subelementos que contiene:

1.  ColorSpace valor de enumeración de cadena restringida de "CIEXYZ"
2.  Elección opcional de WhitePoint NonNegativeXYZType o WhitePointName enumeración de la cadena de los valores D50, D65, A o F2
3.  Geometría GeometryType
4.  Entero de ApertureSize en milímetros

Los valores predeterminados son:

1.  Impresoras RGB y CMYK:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
2.  Escáneres
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
3.  Muestra el dispositivo virtual RGB:
    1.  CIEXYZ MeasurementSpaceType
    2.  WhitePointValue D65
    3.  0/45 GeometryType
    4.  10mm ApertureSize
4.  Cámaras
    1.  CIEXYZ MeasurementSpaceType
    2.  WhitePointValue D65
    3.  GeometryType directo
    4.  10mm ApertureSize

**Condiciones de validación:** La validación de cada subelemento se determina mediante condiciones de validación para esos subelementos. Si falta un subelemento, se usa el tipo de modelo de dispositivo predeterminado específico.

### <a name="geometrytype"></a>GeometryType

String

Valores de enumeración:

-   "0/45"
-   "0/difuso"
-   "difuso/0"
-   Directo

**Condiciones de validación:** Cualquier valor, excepto los valores de enumberation enumerados, no es válido. Esta información no cambiará el comportamiento de procesamiento de línea base.

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

Este elemento es una secuencia de

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="nonnegativecmyksampletype"></a>NonNegativeCMYKSampleType

Este elemento es una secuencia de

1.  CMYK NonNegativeCMYKType
2.  CIEXYZ NonNegativeXYZType

El elemento también tiene una cadena de etiqueta de atributo opcional

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

Este elemento es una secuencia de

1.  RGB NonNegativeRGBType
2.  CIEXYZ NonNegativeXYZType

El elemento también tiene una cadena de etiqueta de atributo opcional

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="nonnegativecmyktype"></a>NonNegativeCMYKType

Este elemento se compone de atributos

1.  C Float
2.  M Float
3.  Float Y
4.  K Float

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

Este elemento se compone de atributos

1.  R Float
2.  G Float
3.  B Float

**Condiciones de validación:** Se debe determinar a partir de los comentarios del sector.

### <a name="extensiontype"></a>ExtensionType

El elemento ExtensionType es una secuencia de cualquier tipo de subelemento y se usa para obtener información de propiedad de aplicaciones que no son de Microsoft.

**Condiciones de validación:** Este elemento es opcional. Puede haber un máximo de 1000 subelementos de extensión.

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

El elemento NonNegativeXYZType se compone de NonNegativeFloatType tres elementos de punto flotante de IEEE de precisión sencilla denominados "X", "Y" y "Z". Estos valores se limitan a los valores de medida de los perfiles DMP. Estas medidas pueden ser absolutas (no relativas) CIEXYZ 1931 valores reflectantes o valores absolutos (no relativos) CIEXYZ 1931 Direct (transpermisivo) en candelas por unidades cuadradas.

**Condiciones de validación:** Solo son válidos los valores del mundo real y los valores de medida CIEXYZ negativos no son válidos. Dado que se trata de valores absolutos, los valores pueden ser mayores que 1,0 f. Un límite razonable para cualquier "X", "Y" o "Z". el valor se establece de forma arbitraria en 10000.0 f.

### <a name="xyztype"></a>XYZType

El elemento XYZType se compone de tres valores de punto flotante de IEEE de precisión sencilla: "X", "Y" y "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Algoritmos de línea de base de CDMP

### <a name="crt-device-model-baseline"></a>Línea de base del modelo de dispositivo CRT

Para entender este modelo, debe tener en cuenta el proceso de caracterización y el modelado de dispositivos. En el proceso de caracterización, las mediciones XYZ se realizan primero en los colores obtenidos al llenar el búfer de pantalla de un dispositivo de pantalla CRT. En los valores de ejemplo siguientes se generarán buenos datos para el modelo de dispositivo CRT de línea base:

Rojo: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutros: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255

También se pueden usar incrementos distintos de 15 y incrementos no lineales. Cada rampa roja, verde, azul y neutra debe contener al menos tres ejemplos, pero se recomienda proporcionar más ejemplos. Debe proporcionar ejemplos de rojo, verde, azul, negro y blanco puros. No es necesario que los ejemplos estén espaciados uniformemente.

El proceso de creación de la matriz de triestímulos consta de dos pasos. En primer lugar, calcule el valor XYZ del punto negro o el flar. Este paso se basa en gran medida en el trabajo de Bernas \[ 3 \] con una función objetiva ligeramente modificada para la optimización no lineal. En segundo lugar, calcule la matriz de triestímulo basada en el resultado del paso uno y, además, desde un cálculo de promedio en todas las medidas por canal, no solo para el número máximo de recuentos digitales.

Cada uno de estos pasos contiene procedimientos detallados. El punto de partida es las rampas (17 pasos en nuestro ejemplo) para cada uno de los canales R, G y B. Cuando las medidas XYZ se representan en el plano *XY* de cromaticidad, se muestra una situación típica en la figura 1. El paso uno consiste en resolver un problema de optimización no lineal para encontrar el punto negro "mejor ajuste" que minimizará el desfase en la cromaticidad a medida que atraviesa los canales R, G y B. Según \[ las Berna 3 \] , buscamos ( *X <sub>k</sub>*,*y <sub>k</sub>*,*Z <sub>k</sub>* ), lo que minimiza la siguiente función objetiva:

![Muestra la función objetiva donde Sr, SG y SB son el conjunto de puntos de datos de los canales R, G y B.](images/cdmp-formula1.png)

donde *s <sub>R</sub>*,*s <sub>G</sub>* y *s <sub>B</sub>* son el conjunto de puntos de datos correspondientes a los puntos de los canales R, G y B. Para *cualquier conjunto, defina:*

![Muestra una fórmula para definir cualquier conjunto.](images/cdmp-formula2.png)

En el ejemplo anterior, \| *s* \| es la cardinalidad de *s*, es decir, el número de puntos del conjunto *S*. ![ Muestra una fórmula para la cromaticidad de un punto.](images/cdmp-formula3.png) es las coordenadas de cromaticidad del punto que ![ muestra un formaula para un punto.](images/cdmp-formula4.png) , de modo que ![ se muestra una fórmula para el promedio o el centro de la masa. ](images/cdmp-formula5.png) , es el promedio, o centro de masa, de todos los puntos del conjunto *S* del plano de cromaticidad. Por lo tanto, ![ muestra una fórmula para la suma de un segundo momento de puntos.](images/cdmp-formula6.png) es la suma de segundos de los puntos del centro de masa y es una medida de cómo se distribuyen los puntos. Por último, ![ muestra una fórmula para la medida total de la distribución de tres clústeres de puntos.](images/cdmp-formula7.png) es una medida total de cómo se distribuyen los tres clústeres de puntos sobre sus respectivos centros de masa.

En el cálculo de se ![ muestra una fórmula de f (X, Y, Z; X KB, YK, ZK).](images/cdmp-formula8.png) , si ![ muestra una fórmula para X. ](images/cdmp-formula9.png) , se omite el cálculo y la cardinalidad de *S* se ajusta en consecuencia.

A pesar de la complejidad aparente de la función de objetivo, es una suma de los cuadrados de muchas funciones de diferenciable en *X <sub>k</sub>*, y *<sub>k</sub>Z <sub>k</sub>* (17 puntos 2 *XY* -Components 3 Channels = 102, en el ejemplo) y, por lo tanto, es receptiva a las técnicas estándar de los mínimos no lineales, como el algoritmo de Levenberg-Marquardt, que es el algoritmo que se Tenga en cuenta que la función de objetivo anterior es diferente de la que se sugiere en Berna \[ 3 en cuanto a \] que la última función mide la varianza de las distancias desde el centro de la masa, de modo que la varianza sea cero cuando los puntos sean equidistantes desde el centro de la masa, incluso aunque puedan repartirse bastante. En el ejemplo, la dispersión de puntos se indica directamente mediante los segundos.

Como con cualquier algoritmo iterativo del problema de los mínimos cuadrados no lineales, Levenberg-Marquardt requiere una estimación inicial. Hay dos candidatos obvios. Uno es (0, 0, 0); el otro es el punto negro medido. En el caso de la CTE, el punto negro medido se usa primero como la estimación inicial. Si se supera un máximo de 100 iteraciones sin alcanzar un umbral de una distancia media de 0,001 de cada punto desde su centro de masa (que corresponde a un valor de umbral de (0,001) 17 3 = 0,000051 para la función de objetivo), se realiza otra ronda de iteraciones con la estimación inicial de (0, 0,0). La estimación resultante del punto negro es XYZ en comparación con la mejor estimación del redondeo anterior de iteraciones (con el punto negro medido como la estimación inicial). Use la estimación que proporciona el valor más pequeño para la función de objetivo. La elección de las iteraciones 100 y la distancia de error de 0,001 se seleccionan de forma empírica. En versiones futuras, podría ser razonable parametrizar la distancia del error.

El resultado del paso uno es el punto negro Estimado ( *X <sub>k</sub>*,*y <sub>k</sub>*,*Z <sub>k</sub>* ). El paso dos consiste en determinar la matriz de triestímulos calculando el promedio de la cromaticidad de los puntos en los tres clústeres obtenidos en el paso uno. En el caso de los CRT, esto se hace principalmente para minimizar los efectos de los errores de medición. Los puntos que se usan para calcular el promedio de la cromaticidad deben ser los mismos puntos que se usan en la optimización del paso uno. En otras palabras, si el primer punto (el recuento digital 15, en el ejemplo) en cada rampa se descarta en el paso de optimización, se debe hacer lo mismo en el promedio. Si ![ muestra fórmulas de cromaticidad promediada para las coordenadas de los canales rojo y verde.](images/cdmp-formula10.png) y ![ muestra una fórmula de cromaticidad promediada para las coordenadas del canal azul.](images/cdmp-formula11.png) son las coordenadas de cromaticidad promedio de los canales rojo, verde y azul; a continuación, el siguiente procedimiento determina la matriz de Triestímulo. En primer lugar, solucione el sistema lineal 3? 3:

![Muestra la primera parte del procedimiento para resolver un sistema lineal de 3? 3.](images/cdmp-formula12.png)

![Muestra la segunda parte del sistema lineal 3? 3.](images/cdmp-formula13.gif)![Muestra el valor b del subscript t al final de la segunda parte del sistema lineal 3? 3.](images/cdmp-formula14.gif)

*X <sub>w</sub>*,*y <sub>w</sub>*,*Z <sub>w</sub>*

![Muestra la parte final del procedimiento para resolver un sistema lineal de 3? 3.](images/cdmp-formula15.png)

Una vez determinada la matriz de triestímulo, la determinación de las curvas de tono sigue el enfoque estándar. En el caso de las pantallas de CRT, se supone que los canales individuales siguen el modelo "GOG":

![Muestra la fórmula del modelo ' G O G '.](images/cdmp-formula16.png)

donde *k <sub>g</sub>* es la "ganancia", 1-*k <sub>g</sub>* es el "desplazamiento" y? es el "gamma". La matriz inversa de la matriz de triestímulo se aplica a los datos XYZ de los neutros para obtener los datos RGB lineales, que después se correlacionan con los valores RGB digitales mediante la regresión no lineal en el modelo GOG. Estas características no tienen que ser las mismas para los canales R, G y B y, por lo general, no son iguales.

Berna \[ 1 \] : los *principios de Billmeyer y Saltzman de la tecnología de color*, 3 <sub>Rd</sub> Ed. John Wiley & hijos (2000).

Berna \[ 2 \] : bernas y Katoh, la función de transferencia digital a radiométrica para monitores de CRT controlados por el equipo, *estándares de color de CIE Expert Symposium ' 97 para la tecnología de creación de imágenes*, noviembre de 1997.

Berna \[ 3 \] : bernas, Fernandez y TAPLIN, estimación de Black-Level emisiones de Computer-Controlled muestra, *investigación de color y aplicación*, 28:379-383 Wiley periódicamente, Inc. (2003)

Kang \[ 1 \] : Kang, *tecnología de color para dispositivos de imágenes electrónicas*, SPIE (1997)

Katoh \[ 1 \] : Katoh, Deguchi y Berna, una caracterización precisa de la propuesta de monitor de CRT (II) para una extensión al método CIE y su comprobación, *OPT. Rev.* 8:397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Línea de base del modelo de dispositivo LCD

La línea de base del modelo de dispositivo LCD es similar a la línea base del modelo de dispositivo CRT. En esta sección se explican las formas en que el modelado de LCD difiere del modelado de CRT.

Una diferencia es que no se puede suponer que las pantallas LCD siguen el modelo GOG que se usa para los CRT, y las curvas de tono se obtienen mediante la interpolación de los datos medidos. Por eso, el eje neutro del dispositivo debe muestrearse con más frecuencia.

Estos son algunos valores de ejemplo típicos que pueden generar buenos datos para la línea de base del modelo de dispositivo LCD:

Rojo: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutros: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

El proceso de calcular el promedio de los colores de color medidos para obtener las cromacidads de las principales del dispositivo es más importante para los monitores de LCD que para los CRT. Cuando las medidas XYZ se representan en el plano *XY* de cromaticidad, se muestra una situación típica en la figura 1. Observe cómo se desplaza la cromaticidad hacia el punto negro. Esto se debe a que todas las pantallas LCD tienen una cierta cantidad de fugas ligeras.

![Diagrama que muestra un gráfico de la cromaticidad usando datos sin procesar sin corrección.](images/cdmp-lcd-dmp-figure1.png)

**Figura 1** : Diagrama de cromaticidad con datos sin procesar sin corrección

Cuando se resta de las medidas de XYZ sin procesar, se muestra una situación típica en la figura 2. Ahora, los puntos están agrupados en clústeres de tres centros, aunque no son idénticos en ellos. El proceso de promedio descrito para los CRT mejora en gran medida los resultados de las pantallas LCD.

![Diagrama que muestra un gráfico de la cromaticidad usando datos sin procesar con un punto negro ajustado.](images/cdmp-lcd-dmp-figure2.png)

**Figura 2** : el diagrama de cromaticidad con datos con el punto negro ajustado

### <a name="rgb-capture-device-model-baseline"></a>Línea de base del modelo de dispositivo de captura RGB

El modelo de dispositivo de captura RGB de línea base es una subclase de la clase IDeviceModel. En la caracterización colorimétrica de los dispositivos de captura de color, como los escáneres y las cámaras digitales, se usa el enfoque siguiente. Un destino compuesto por revisiones de color con valores de CIEXYZ conocidos se captura mediante el dispositivo de captura. El resultado de la captura es una imagen de mapa de bits RGB en la que el color de cada revisión se codifica en un valor RGB. Estos valores RGB de dispositivo son específicos de un dispositivo de captura determinado. El objetivo de la caracterización colorimétrica es establecer una relación empírica entre los valores RGB del dispositivo y los valores CIEXYZ, o una transformación matemática de RGB a XYZ que se modele de la forma más precisa posible del comportamiento del dispositivo de captura.

Este tipo de transformación matemática se puede modelar razonablemente mediante polinomiales de bajo grado. Este procedimiento se detalla en la literatura, por ejemplo, Kang \[ 92 \] , Kang \[ 97 \] . En Kang \[ 97 \] , se genera un enfoque que utiliza un conjunto de tres polinómicas con 3, 6, 8, 9, 11, 14 o 20 términos en las variables R, G y B, mientras que las tres regresión polinómicas están respectivamente en los componentes X, Y y Z del espacio CIEXYZ. En el caso de la Polinómico de 20 términos, el formulario es:

![Muestra el Polinómico de 20 términos.](images/cdmp-formula20.png)

Hay expresiones similares para y y Z. La técnica matemática para ajustar los polinómicos se encuentra dentro de "regresión lineal multivariada" y se describe en cualquier texto elemental en las estadísticas.

Este método de regresión lineal sufre que no se minimice la función de objetivo "derecho". Por diseño, la regresión lineal encuentra la solución de los mínimos cuadrados, lo que implica que los coeficientes obtenidos reducirán la suma total de los cuadrados de los errores en el espacio subyacente, o equivalentes, la suma de los cuadrados de las distancias euclidiana. En la práctica, desea minimizar la suma de los cuadrados de? Es, ¿dónde? E es uno de los estándares aceptados, como CIE94. Minimizar esta función de objetivo es un problema de regresión no lineal.

En el nuevo motor, Lab to XYZ es el espacio de colores CIE en el que se retrasan y se usa el polinomial cúbico de 20 términos como modelo para el dispositivo de captura, o coeficientes LS, como, como BS, de modo que las siguientes polinomias minimicen la suma de los cuadrados de? E <sub>CIE94</sub> s.

![Muestra un conjunto de fórmulas polinómicas.](images/cdmp-formula21.png)

La solución ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) en el espacio numérico real de la dimensión 60 **R** 203 debe ser tal que se minimice el siguiente error total:

![Muestra el error total que se va a minimizar.](images/cdmp-formula22.png)

donde la suma se realiza a través de todos los pares de puntos de datos (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) en el conjunto de datos muestreado, además de los puntos de control adicionales que se detallan a continuación. Se trata de un problema de regresión no lineal porque los parámetros *?<sub> i</sub>*, *<sub>i</sub>*, * <sub>i</sub>* entrar en la función de objetivo de una manera no lineal (no es cuadrática).

Dado que la función de objetivos ¿es una función no lineal (y no cuadrática) de los parámetros *?<sub> i</sub>*, *<sub>i</sub>* y * <sub>i</sub>*, debe recurrir a técnicas iterativas para solucionar el problema de optimización. Dado que la forma de la función Objective es una suma de cuadrados, se usa una técnica de optimización estándar denominada algoritmo Levenberg-Marquardt. Se considera el método preferido para los problemas con menos líneas de cuadrados. Para los algoritmos iterativos como Levenberg-Marquardt, debe proporcionar una estimación inicial. Una buena estimación inicial suele ser fundamental para buscar el valor mínimo correcto. En este caso, una buena candidata para la estimación inicial es la solución del problema de regresión lineal. En primer lugar, minimice la suma del cuadrado de las distancias de euclidiana en el espacio de laboratorio, definiendo una función de objetivo cuadrático:

![Muestra una función de objetivo cuadrático definida.](images/cdmp-formula23.png)

La solución matemática a este problema de "mínimos cuadrados lineales" es muy conocida. Porque *?<sub></sub>solo aparece* en el modelado *L* , solo aparece en el modelado *u* *, y <sub></sub>* * <sub>i</sub>* solo aparece en el modelado *v* ; el problema de optimización se puede descomponer en tres subproblemas: uno para *L*, uno para *u* y otro para *v*. Considere las ecuaciones *L* . (Las ecuaciones *u* y las ecuaciones *v* siguen exactamente el mismo argumento). El problema de minimizar la suma de los cuadrados de los errores en *L* puede indicarse como resolver la siguiente ecuación de matriz en el sentido de los mínimos cuadrados:

![Muestra una ecuación de matriz para L.](images/cdmp-formula24.png)

donde *N* es el número total de puntos de datos (puntos muestreados originales más puntos de control creados de la manera que se describe a continuación). Normalmente, *N* es mucho mayor que 20, por lo que se determina la ecuación anterior, lo que requiere una solución con menos cuadrados. Una solución de formulario cerrado para **?** está disponible:

![Muestra una solución de formulario cerrada.](images/cdmp-formula25.png)

En la práctica, no se usa la evaluación directa mediante la solución de formulario cerrado porque tiene propiedades numéricas deficientes. En su lugar, se aplica un tipo de algoritmo de factorización de matriz a la matriz de coeficientes, lo que reduce el sistema de ecuaciones a un formato canónico. En la implementación actual, se aplica la descomposición de valores singular (SVD) a la matriz **R** y, a continuación, se resuelve el sistema descompuesto resultante.

La solución al problema de regresión lineal, indicada por ![ muestra la solución al problema de regresión lineal.](images/cdmp-formula26.png) , se usa como punto inicial del algoritmo Levenberg-Marquardt. En este algoritmo, se calcula un paso de prueba que debe ir más cerca de la solución óptima. El paso de prueba satisface un conjunto de ecuaciones lineales que dependen del valor funcional y de los valores de los derivados en el punto actual. Por esta razón, los derivados de la función Objective? ¿con respecto a los parámetros *?<sub> i</sub>*, *se <sub></sub> <sub></sub>* necesitan entradas para el algoritmo de Levenberg-Marquardt. Aunque hay 60 parámetros, hay un acceso directo que le permite calcular mucho menos. Por la regla de cadena de cálculo,

![Muestra una ecuación que permite usar un acceso directo mediante la regla de cadena de cálculo.](images/cdmp-formula27.png)

donde *j* = 1, 2, 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* es el valor CIELab del punto de ejemplo *i* TH y *r <sub>ij</sub>* es la entrada (*i*,*j* ) de la matriz **R** definida anteriormente. Por lo tanto, en lugar de calcular los derivados para los parámetros 60, puede calcular los derivados de *L*,*a* y *b* mediante la diferencia de avance numérica.

También es necesario configurar un criterio de detención para los algoritmos iterativos. En la implementación actual, las iteraciones se terminan si el DECIE94 cuadrado medio es menor que 1, o el número de iteraciones realizadas ha superado 10. El número 10 procede de la experiencia práctica de que, si las primeras iteraciones no reducen el error de forma significativa, las iteraciones posteriores no ayudarán a evitar que se mueva el punto de una manera oscilante, es decir, el algoritmo no puede converger. Incluso en el caso de que el algoritmo difiera, podemos estar seguros de que el DECIE94 no es peor que lo que iniciamos, es decir, con los parámetros obtenidos de la regresión lineal.

Incluso con el método anterior de regresión no lineal, hay varios problemas con la conexión. Uno de los problemas es que los polinómicos tienden a sobrepasar o a superar los puntos de datos. Es posible que se introduzcan los máximos y mínimos artificiales en el proceso de instalación. Esto se puede compensar mediante el uso de polinomiales de bajo grado, que es el motivo por el que no debe usar más de tres grados. Un aspecto más grave del exceso o el subintento es que, mientras que un polinomio puede tomar cualquier valor real teóricamente, el espacio que intenta modelar normalmente tiene restricciones físicas y restricciones prácticas. CIEXYZ debe tener todos los valores X, Y, Z no negativos, que es una restricción física. En la práctica, solo toman valores en la magnitud de cientos, no en miles o más. Del mismo modo, CIELAB o CIELUV tiene sus propias restricciones físicas y prácticas. Cuando el espacio RGB se rellena con puntos de ejemplo, el problema de un exceso o un subgrave no es serio. Sin embargo, los puntos RGB capturados desde el dispositivo de captura no suelen llenar el espacio RGB de manera uniforme. Los puntos solo pueden rellenar el 80% del cubo RGB, o peor, pueden residir en un conjunto de un conjunto de dimensiones inferior. Cuando esto sucede, los polinómicos con regresión pueden hacer un trabajo pobre en la extrapolación de los valores más allá de los puntos de datos, a veces devolviendo predicciones no reareales. Desea un modelo que siempre devuelva valores realistas razonablemente. Esto requiere un método que pueda controlar eficazmente el comportamiento del límite de los polinómicos de regresión imponiendo costos adicionales a esos polinómicos que se comportan de forma errática cerca del límite del cubo RGB. Una medida adicional para asegurarse de que los polinomiales siempre devuelven valores realistas se aplican recortando la salida a dentro del raíz espectral de CIE.

En este punto, el modelado del escáner y el modelado de la cámara difieren entre sí. Se espera que el modelo de cámara se extrapola a regiones más allá de los puntos muestreados, incluido el "reflejos especulares", la misma extrapolación no es necesaria para el modelo de escáner. Se espera que el destino del escáner cubra una caracterización similar a la de los materiales impresos que se van a examinar. Todavía es necesario que el modelo del escáner sea robusto en el sentido de que no debe devolver valores no reales, pero no se requiere la extrapolación más allá del destino de la caracterización. Para garantizar la solidez, la L polinómica anterior se recorta en 100, es decir, el modelo Polinómico se fuerza a no extrapolar más allá de "DMín" del destino del escáner.

Se espera que el modelo de cámara se extrapolar a las iluminaciones especulares, por lo que no se desea recortar en 100. En su lugar, se utiliza el algoritmo siguiente.

Los puntos de control artificiales se introducen para controlar el comportamiento de los polinómicos en regiones con un muestreo insuficiente. Mediante la colocación estratégica de estos puntos de control con los valores adecuados, sirven para "extraer" los polinómicos en la dirección requerida. En la implementación actual, se usan ocho puntos de control correspondientes a las esquinas del cubo RGB. Si los valores del dispositivo se normalizan en Unity, estos puntos son:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

Excepto en el caso de *R*  = *G*  = *p* = 1 blanco que está asociado a un valor CIELAB de *L* = 100, *u*  = *v* = 0, se usa el algoritmo de extrapolación siguiente para determinar el valor de CIELab adecuado con el que se va a asociar. Por lo general, para un determinado (*r*,*g*,*b* ), se asocia una ponderación a cada uno de los (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ) del conjunto de datos muestreado. Hay dos objetivos para asignar el peso. En primer lugar, el peso es inversamente proporcional a la distancia entre (*r*,*G*,*B* ) y (*R <sub>i</sub>*,*G <sub>i</sub>*,*b <sub>i</sub>* ). En segundo lugar, desea descartar o asignar el peso 0 a, los puntos que tienen un matiz diferente que el punto especificado (*R*,*G*,*B* ). Para tener en cuenta el matiz, considere los puntos que se encuentran dentro de un cono cuyo vértice está en (0,0), cuyo eje coincide con la línea que se une (0, 0,0) a (*R*,*G*,*B* ) y cuyo ángulo semivertical? cumple los Co? = 0,9. Vea la figura 3 para ver una ilustración de este cono.

![Diagrama que muestra la forma del entorno.](images/cdmp-lcd-dmp-figure3.png)

**Figura 3** : filtrado de los puntos de ejemplo por ángulo y distancia. La forma del entorno representado solo es para fines ilustrativos. La forma real depende de la distancia utilizada. es un entorno en forma de rombo si se usa la norma 1.

Dentro de este cono, se realiza un segundo filtrado que se basa en la distancia RGB, que utiliza la norma 1, definida por

![Muestra la fórmula para el segundo filtrado dentro del cono.](images/cdmp-formula28.png)

Con el cono actual, la búsqueda inicial es para los puntos que se encuentran dentro de una distancia de 0,1 (*R*,*G*,*B* ). Si no se encuentra ningún punto dentro de este radio, el radio aumenta en 0,1 y la búsqueda se reinicia. Si en las siguientes redes de redondeo no hay ningún punto, el radio aumenta en 0,1. Este proceso continúa hasta que el radio supera MaxDist/5, donde MaxDist = 3, en el caso de 1-norma. Si no se encuentra ningún punto, el cono se amplía reduciendo la CES? por 0,05, es decir, al aumentar el ángulo? y reinicie todo el proceso con un radio en aumento. Este proceso continúa hasta que se encuentra un conjunto de puntos no vacío o cos? llega a 0, es decir, el cono se ha abierto hasta convertirse en un plano. En este punto, la búsqueda se reinicia aumentando el radio, salvo que la búsqueda continúa hasta que el radio llega a MaxDist. Esto garantiza que, en el peor de los casos, se encontrará un conjunto de puntos no vacío. El algoritmo se resume en el diagrama de flujo de la figura 4.

![Diagrama que muestra el flujo del algoritmo.](images/cdmp-lcd-dmp-figure4.png)

**Figura 4** : Diagrama de flujo para determinar los conjuntos de puntos de ejemplo usados en la extrapolación para un valor RGB de entrada

Suponiendo que el proceso anterior produce *un conjunto de* puntos no vacíos (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) y el correspondiente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), para cada uno de estos puntos, se asigna una ponderación *w <sub></sub>* , proporcionada por

![Muestra la fórmula para una ponderación de cada punto.](images/cdmp-formula29.png)

Por último, el extrapolant se define mediante

![Muestra la definición de extrapolant.](images/cdmp-formula30.png)

Las ecuaciones anteriores constituyen una instancia de los "métodos ponderados de distancia inversa", que normalmente se denominan métodos Charlene. Al ejecutar cada uno de los ocho puntos de EQ (6) a través del algoritmo, se obtienen ocho puntos de control, cada uno con los valores *R*,*G*,*B* y *L*,*a* y *b* , que se colocan en el grupo con los datos de ejemplo originales.

Para asegurarse de que el modelo siempre genera valores de color válidos y para la integridad del sistema y la estabilidad en toda la canalización de procesamiento de color, debe realizar un recorte final en la salida del modelo polinómico. El componente achromatic (*y* o *L* ) y el componente cromático (*XY* o *a'b*, que están relacionados con el espacio XYZ mediante una transformación proyectada) describen la gama visual CIE. En la implementación actual, se usa la cromaticidad de *a'b* porque está directamente relacionada con el espacio CIELUV. Para cualquier valor de *CIELAB* , primer clip *L* en un valor no negativo:

![Muestra el recorte de L en un valor no negativo.](images/cdmp-formula31.png)

Para permitir la extrapolación de los reflejos especulares, *l* no se recorta en 100, el límite superior "convencional" para *L* en el espacio de laboratorio.

Después, si *L* = 0, a *y* *b* se recortan de modo que a *= b =* 0. Si es *L* ? 0, calcular

![Muestra la fórmula si L = 0.](images/cdmp-formula32.png)

Estos son los componentes de un vector en el diagrama de *a'b* desde el punto blanco (*u? '*,*v? '* ) al color en cuestión. Defina el raíz espectral de CIE como el casco convexo de todos los puntos (*a '*,*b '* ), parametrizado por la longitud de onda?:

![Muestra la fórmula para la longitud de onda.](images/cdmp-formula33.png)

donde ![ muestra las funciones para la coincidencia de color de CIE.](images/cdmp-formula34.png) son las funciones de coincidencia de color de CIE del observador de 2 grados. Si el vector está fuera del raíz de CIE, el color se recorta hasta el punto en el raíz de CIE que es la intersección de raíz y la línea definida por el vector. Vea la figura 5. Si se ha producido un recorte, se reconstruye el valor *a* y *b* restando primero *a? '* y *b? '* del recorte *a '* y *b '* y, a continuación, multiplicar por 13 *L*.

![Diagrama que muestra el gráfico para el algoritmo de recorte.](images/cdmp-lcd-dmp-figure5.png)

**Figura 5** : algoritmo de recorte para los valores de laboratorio que se encuentran fuera de la gama visual de CIE

En la implementación actual, el raíz espectral de CIE en el plano *a'b* se representa mediante una curva lineal a trozos con segmentos 35 (que corresponde a una longitud de onda de 360 nm a 700 nm inclusive). Mediante el orden de los segmentos de línea para que sus ángulos subpuestos en el punto blanco sean ascendentes, lo que equivale a las longitudes de onda descendentes, el segmento de línea que forma una intersección con el rayo formado por el vector anterior se puede encontrar mediante una búsqueda binaria simple.

### <a name="rgb-printer-device-model-baseline"></a>Línea base del modelo de dispositivo de impresora RGB

Una caracterización de dispositivos de una impresora RGB consiste en construir un modelo empírico del dispositivo que predice el color CIELUV independiente del dispositivo para cualquier valor RGB determinado.

Hay dos maneras de construir el modelo empírico. Una manera es usar los datos del dispositivo para una impresora RGB y el otro es usar datos de parámetros analíticos. En el primero, los datos de medición proporcionados por un usuario para un dispositivo de impresora RGB se usan para crear una tabla de búsqueda en 3D (LUT). Los datos de medición se componen de valores XYZ para revisiones RGB muestreadas uniformemente. Los tamaños de muestreo típicos son 9 o 17 para cada componente. Cada revisión se mide con un colorimeter o un espectrofotómetro en el espacio CIEXYZ. El valor XYZ para una revisión se convierte a continuación en el valor CIELUV, formando un LUT 3D. En el modelo de dispositivo, el método de interpolación tetrahedral de Sakamoto se aplica a la LUT 3D para predecir los datos CIELUV para un dato RGB determinado. (Conviene la patente 4275413 de EE. UU. (Sakamoto et al.), patentes de EE. UU. 4511989 (Sakamoto), Kang \[ 1 \] . Las dos patentes mencionadas han expirado.). Los datos de parámetros analíticos pasados en el segundo método son simplemente un LUT que se compiló anteriormente. Normalmente, la LUT se compiló con el primer método, aunque podría estar compilada a mano.

En la administración del color actual, el mapa de origen se define como la asignación que va desde el espacio RGB a un espacio de colores de CIEXYZ independiente del dispositivo. El mapa de destino se define como la asignación que va del espacio de colores CIEXYZ independiente del dispositivo al espacio RGB. Es el inverso del mapa de origen.

El modelo empírico se usa directamente en el mapa de origen. En primer lugar, asigna los datos RGB especificados a los datos de CIELUV, que se convierten en datos XYZ. En el mapa de destino, los datos de CIEXYZ independientes del dispositivo se convierten primero en datos CIELUV. A continuación, se usan el modelo empírico y el método de Newton-Raphson clásico para predecir los mejores datos RGB para los datos de CIELUV. Los detalles sobre la conversión de los datos de CieLUV a RGB son los siguientes:

Después de generar un LUT 3D de RGB a CieLUV, el mapa de RGB a LUV se crea con la interpolación tetrahedral en RGB. Este mapa se indica mediante las ecuaciones siguientes:

![Muestra las ecuaciones del mapa de R G B a L U V.](images/cdmp-image125.png)

La inversión de la asignación consiste en resolver, para cualquier color. ![Muestra L U V.](images/cdmp-image127.png) , el siguiente sistema de ecuaciones no lineales:

![Muestra las ecuaciones no lineales para lolving cualquier color L U V.](images/cdmp-image129.png)

En la nueva CTE se usa una ecuación no lineal que se basa en el método de Newton-Raphson clásico. Una estimación inicial o *una priori* See, s <sub>anteriores</sub> -(R 0, G 0, B 0) se obtiene al buscar en una "matriz de inicialización" que se compone de una cuadrícula de 8x8x8 uniforme de pares precalculados (RGB, Luv). Se elige el Luv de RGB correspondiente más cercano a la L \* u \* v \* . Cada punto de la matriz de inicialización corresponde al centro de una celda para que las iteraciones no empiecen por un punto en la superficie del límite del cubo RGB. En otras palabras, el RGB de las semillas se define mediante: paso = 1/8 s <sub>ijk</sub> = (paso/2 + (i-1) paso, paso/2 + (j-1) paso, paso/2 + (k-1) paso) con i, j, k = 1... 8 en el paso *i* de Newton-Raphson, la siguiente estimación ![ muestra las variables de la siguiente estimación.](images/cdmp-image133.png) se obtiene mediante la fórmula:

![Muestra la fórmula para la estimación.](images/cdmp-image135.png)

La iteración se detiene cuando el error (distancia en el espacio CIELUV) es menor que un nivel de tolerancia preestablecido (0,1 en la CTE) o cuando el número de iteraciones ha superado el número máximo permitido de iteraciones (10 en la CTE). Los valores de la tolerancia y el número de iteraciones se han determinado empíricamente como efectivos. En versiones futuras, se puede cambiar el valor de tolerancia.

La matriz Jacobian se calcula utilizando la diferencia hacia delante, excepto en un punto límite (una o varias de las R, G, B es 1) donde se usa la diferencia hacia atrás en su lugar. En lugar de calcular el inverso de la matriz Jacobian, el sistema lineal se resuelve directamente utilizando Gauss-Jordan eliminación con dinamización completa.

Al final de las iteraciones, es posible que no se logre la convergencia porque Newton-Raphson es un algoritmo "local", es decir, solo funciona bien si comienza con una estimación inicial cercana a la solución real. Si, al final de la Newton-Raphson las iteraciones, no se ha logrado la convergencia dentro de la tolerancia a errores definida previamente, las iteraciones se reinician con un nuevo conjunto de inicializaciones, que se define de la siguiente manera.

Por ejemplo, la mejor solución obtenida hasta ahora es (r, g, b). En esta solución, se derivan N inicializaciones posteriores, donde N = 4. Intuitivamente, la solución se mueve "hacia el centro" en un tamaño de paso que depende de N. Vea la figura 6.

![Diagrama que muestra las direcciones Perturbation de la solución.](images/cdmp-image136.png)

**Figura 6** : la dirección Perturbation de la solución depende de la octeto en la que se encuentra.

En otras palabras, si r &gt; 0,5, se reduce el valor del canal r; de lo contrario, se aumenta el valor. Existe una lógica similar para los canales G y B. Las definiciones precisas son:

PERTURBATION = 0.5/(N + 1)

DIR (r) =-1 si r &gt; 0,5; + 1 en caso contrario. De forma similar para DIR (g) y DIR (b)

JTH a posteriori SEED, s????, es (r + DIR (r) \* j \* PERTURBATION, g + DIR (g) \* j \* PERTURBATION, b + DIR (b) \* j \* PERTURBATION)

Pruebe los primeros???? y si proporciona una nueva solución dentro de la tolerancia a errores, puede detenerse. En caso contrario, pruebe los segundos???? y así sucesivamente hasta el n????.

Los esquemas de todo el algoritmo se muestran en la figura 7.

![Diagrama que muestra el flujo para invertir el modelo de dispositivo.](images/cdmp-image138.png)

**Figura 7** : esquemas de invertir el modelo de dispositivo

### <a name="rgb-virtual-device-model-baseline"></a>Línea base de modelo de dispositivo virtual RGB

Este modelo de dispositivo (DM) es un algoritmo de reproducción de matriz/tono simple. La matriz se deriva del punto blanco y de los primarios mediante algoritmos de ciencia de color estándar. La curva de reproducción de tono se deriva de los parámetros de medida según las descripciones de ICC de CurveType y ParametricType (o invertido según sea necesario). Los detalles de los algoritmos internos se proporcionarán después de la validación adicional de problemas de intervalo dinámico elevados.

El modelo de dispositivo virtual RGB es una curva de reproducción de matriz/tono ideal similar al diseño de perfil basado en la matriz de tres componentes de ICC. Los parámetros de "medida virtual" del DM incluyen un valor de punto blanco (CIEXYZ absoluto), valores principales de RGB (CIEXYZ absoluto) y una curva de reproducción de tono que se basa en la ParametricCurveType ICC y CurveType en formato XML coherente con los esquemas DMP.

En la tabla siguiente se muestran la codificación de tipo de función parametricCurveType de ICC y la compatibilidad correspondiente en IRGBVirtualDeviceModelBase.



| Tipo de función                                         | Parámetros                          | Tipo                                     | Nota:                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Muestra la función ' GammaType '.](images/cdmp-image154.png)<br/> | e<br/>              | GammaType<br/>                 | Implementación común<br/>           |
| ![Muestra la función ' GammaOffsetGainType '.](images/cdmp-image156.png)<br/> | GA b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![Muestra la función ' GammaOffsetGainOffsetType '.](images/cdmp-image158.png)<br/> | GA b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![Muestra la función ' GammaOffsetGainGainType '.](images/cdmp-image160.png)<br/> | GA b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2.1<br/> sRGB<br/> |
| ![Muestra una función para los parámetros ' g a b c d e f '.](images/cdmp-image162.png)<br/> | GA b c e f<br/>   | N/D<br/>                       | No se admite en WCS<br/>            |



 

La curva de tono para dispositivos virtuales RGB se aplica en DeviceToColorimetric entre los datos de entrada, pDeviceColors y la multiplicación de la matriz. En el caso de ColorimetricToDevice, se debe usar un método para invertir la curva de tono. En la implementación de línea de base, esto se realiza mediante la interpolación directa en la misma curva de tono que se usa para DeviceToColorimetric.

Las curvas se deben especificar en los perfiles como pares de números en el espacio float. El primer número representa los valores de pDeviceColors. El segundo número representa la salida de la curva de tono. Todos los valores de la curva de tono deben estar entre minColorantUsed y maxColorantUsed. Las curvas de tono deben contener al menos dos entradas: una para minColorantUsed y otra para maxColorantUsed. El número máximo de entradas en el ToneCurve es 2048. En general, cuanto mayor sea el número de entradas de la tabla, más precisa podrá modelar la curvatura. Se realiza una interpolación lineal a trozos entre las entradas.

Puede considerar métodos de interpolación alternativos. Si sabe algo sobre el comportamiento subyacente del dispositivo, puede usar menos muestras y modelo con más precisión con una curva de orden superior. Pero si usa un tipo de curva incorrecto, será muy poco preciso. Sin más información, no puede adivinar el tipo de curva. Por lo tanto, use la interpolación lineal y proporcione muchos puntos de datos.

### <a name="cmyk-printer-device-model-baseline"></a>Línea de base del modelo de dispositivo de impresora CMYK

Una caracterización de dispositivos de una impresora CMYK consiste en construir un modelo empírico del dispositivo que predice el color impreso para cualquier valor CMYK determinado. La caracterización también incluye la inversion de este modelo para que se pueda imprimir una receta del valor CMYK para un color determinado. Normalmente se define en términos de CIEXYZ o CIELAB.

Normalmente, se utiliza un destino 8.7/3 que contiene revisiones CMYK. Las revisiones consisten en el muestreo del espacio CMYK de una manera bien definida para que se forme una cuadrícula rectangular (con un espaciado no uniforme en C, M, y y K). Después, cada revisión se mide con un colorimeter o un espectrofotómetro. Las medidas en los valores CIEXYZ forman una tabla de búsqueda (LUT), de la que se crea un modelo empírico de la impresora mediante el método de interpolación de Sakamoto. Patentes 4275413 de EE. UU. (Sakamoto et al.), patentes de EE. UU. 4511989 (Sakamoto), Kang \[ 1 \] . Las dos patentes mencionadas han expirado.

Los requisitos específicos para los ejemplos de medida CMYK necesarios para que un perfil de modelo de dispositivo se acepte como válido por el modelo de dispositivo de línea de base de impresora CMYK son los siguientes. (El conjunto de ejemplo se describe con mayor claridad como un conjunto de cubos de ejemplo CMY, cada uno asociado a un nivel K específico).

-   Como mínimo, se deben proporcionar cubos CMY válidos para los niveles K = 0 y K = 100.
-   Los niveles K intermedios pueden tener un espaciado no uniforme.
-   Se omitirá cualquier nivel K intermedio sin un cubo CMY válido.
-   Los cubos CMY pueden utilizar intervalos de muestra no uniformes (espaciado de cuadrícula), pero el mismo conjunto de intervalos de muestra debe usarse en todas las dimensiones C, M e y del cubo CMY para un nivel K determinado.
-   Cada cubo CMY de nivel K puede usar un número y espaciado diferentes de intervalos de muestra.
-   Todos los cubos CMY deben contener las "esquinas" del cubo CMY, es decir, los ejemplos de CMY en \[ 0, 0, 0, \] \[ 0, 0100 \] , \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100.100 \] , \[ 100, 0100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .
-   Cualquier nivel intermedio de la cuadrícula CMY debe ser totalmente muestreado en cada canal. En otras palabras, debe existir un ejemplo en cada intersección de cuadrícula 3D dentro del cubo CMY.
-   En el caso de los cubos K = 0 y K = 100 CMY, los cubos de 2x2x2 "solo esquinas" son los mínimos aceptados como válidos.

    \[Nota: para K = 0 y K = 100 niveles, se procesará un cubo de 3x3x3 CMY como un cubo 2x2x2 "Corners-Only". se omite el nivel de ejemplo intermedio. en los cubos de 4x4x4 y más grandes se utilizarán todos los ejemplos de la cuadrícula.\]

-   En el caso de los niveles K intermedios, los cubos de 4x4x4 CMY son los mínimos aceptados como válidos.

Un perfil de alta calidad usará cuadrículas de muestreo más precisas que la mínima necesaria para la validez, normalmente 9x9x9x9 o superior. Los ejemplos de los dispositivos de ti 8.7/3, IT 8.7/4 y ECI generan perfiles de modelo de dispositivo (DMPs) válidos para el modelo de dispositivo de línea de base de impresora CMYK. Aunque este modelo de dispositivo puede pasar por alto los ejemplos superfluos (fuera de la cuadrícula) en estos destinos, no se garantiza que pueda hacerlo para otros destinos y, por lo tanto, se recomienda que se quiten los ejemplos extraños de los conjuntos de medidas que entran en los perfiles de este modelo de dispositivo.

La inversión del modelo de impresora presenta más dificultades. Dado un color de entrada en CIECAM, hay una pregunta que indica si este color está dentro de la gama de la impresora. También hay un problema con respecto a la organización de puntos en el espacio de apariencia de color. Aunque podemos organizar los valores CMYK para que aparezcan en una cuadrícula rectangular, tal y como se hace en el destino 8.7/3, no se puede decir que los colores impresos resultantes se encuentran en el espacio de apariencia del color. En general, están dispersos en el espacio de apariencia de color sin un patrón determinado.

Por lo general, hay dos enfoques para el problema de inversion de puntos dispersos. Un enfoque consiste en usar una subdivisión geométrica de la gama de impresoras con sólidos de 3 dimensiones elementales, como tetrahedra. Una subdivisión de la gama de la impresora en el espacio de apariencia del color puede ser inducida por la Subdivisión correspondiente del espacio CMY (K), consulte bloqueo \[ 93 \] , Kang \[ 97 \] . Este enfoque tiene la ventaja de la simplicidad computacional. En el caso de Tetrahedron, solo se usan cuatro puntos en una interpolación. Por otro lado, el resultado depende en gran medida de unos cuantos puntos, lo que significa que un error de medición tendrá un efecto significativo en el resultado. Interpolant también tiende a no ser tan suave. El segundo enfoque no supone ninguna subdivisión y se basa en la técnica de interpolación de datos diseminada. Un ejemplo clásico es la técnica de la interpolación Charlene o el método ponderado inverso (consulte Charlene \[ 68 \] ). En este caso, se eligen varios puntos que rodean el punto de entrada de alguna manera, cada uno asignado a una ponderación, normalmente inversomente proporcional a la distancia, y el interpolant se toma como la media ponderada de los puntos vecinos. En este enfoque, la elección de puntos contiguos es fundamental para el rendimiento. Aunque los pocos puntos pueden representar el interpolant inexacto y no Smooth, demasiados puntos imponen un elevado costo de cálculo, ya que las ponderaciones suelen ser funciones no lineales y costosas de calcular.

Los dos enfoques descritos anteriormente tienen problemas. El enfoque de subdivisión depende de los datos que sean razonablemente nulos de ruido y, por lo general, el interpolant no es muy suave. La interpolación de datos diseminada es más tolerante al ruido de los datos y, por lo general, proporciona un interpolant más suave, pero es computacionalmente más caro.

La nueva CTE toma un enfoque alternativo. El dispositivo CMYK se trata como una colección de varios dispositivos CMY, cada uno de los cuales tiene un valor específico de negro (K). El uso de un algoritmo de selección que toma como luz y intensidad de los parámetros se elige un nivel de negro. Los valores CMY se obtienen mediante la inversion de la tabla de CMY a Luv correspondiente con los métodos de Newton utilizados en otra parte por el algoritmo de impresora RGB.

Siga los pasos que se describen a continuación.

1.  Imprime el destino de la caracterización, que es el destino 8.7/3, o un destino que contiene el muestreo del espacio CMYK con intervalos de espaciado frecuente o irregular.
2.  Mida el destino mediante un espectrofotómetro y convierta las medidas en el espacio de CIELUV.
3.  Construya el mapa hacia delante de CMYK a Luv.
4.  Use el mapa de avance para construir un conjunto de Luv para un intervalo de valores K.
5.  Para cualquier valor de Luv de entrada, el valor CMYK correspondiente se obtiene seleccionando uno de los mapas construidos en el paso 4 anterior e invirtiendo con el método de Newton para obtener un conjunto de Colorant CMY que acompañe al valor K seleccionado.

Los pasos 1 y 2, que son procedimientos estándar, los realiza un programa de generación de perfiles que no forma parte de la nueva CTE. El destino 8.7/3 contiene un muestreo razonablemente detallado de todos los valores CMYK en distintos niveles de C, M, y y K. como alternativa, se puede usar un destino personalizado con un muestreo uniforme de los canales C, M, y y K. Una vez que se imprime el destino, se puede usar un espectrofotómetro o colorimeter para medir el valor XYZ de cada revisión y el valor XYZ se puede convertir al valor Luv mediante el modelo CIELUV.

El paso 3, la construcción del mapa hacia delante de CMYK a Luv, se puede lograr aplicando cualquier técnica de interpolación conocida, como un método multilineal o tetrahedral, en la cuadrícula rectangular en el espacio CMYK. En la nueva CTE, se usa una interpolación tetrahedral de 4 dimensiones. Dado que las cuadrículas de muestreo de CMY suelen ser diferentes en cada nivel de K, sin embargo, usamos una técnica de supermuestreo, tal y como se detalla a continuación. En el caso de un punto CMYK determinado, los niveles de la sandwich se determinan en primer lugar en función del valor K. A continuación, introduzca una "supercuadrícula" en cada nivel K que sea una Unión de las cuadrículas de CMY en cada uno de los dos niveles de K. En cada nivel K, el valor Luv de cualquier punto de cuadrícula recién introducido se obtiene mediante una interpolación tetrahedral tridimensional dentro de ese nivel K. Por último, en esta nueva cuadrícula se realiza una interpolación tetrahedral de 4 dimensiones para el punto CMYK específico.

![Diagrama que muestra el supermuestreo.](images/cdmp-image163.png)

**Figura 8** : supermuestreo

El paso 4 crea un conjunto de tablas de búsqueda de CMY a Luv (LUTs). El mapa hacia delante construido en el paso 3 se llama repetidamente para volver a muestrear el espacio CMYK. El espacio de colores CMYK se muestrea con un espaciado uniforme de K y otro, pero sigue uniformemente espaciado, muestreo de CMY.

El paso 5 es un procedimiento para obtener el valor CMYK mediante el LUTs construido en el paso 4 para cualquier punto de Luv de entrada. El valor adecuado de K se elige mediante el análisis de la luminosidad y el grado de color de la Luv solicitada. Una vez seleccionada la tabla, los valores CMY se obtienen de la tabla mediante el método de Newton (como se documenta en el modelo de dispositivo de impresora RGB anterior).

El espacio CIELUV se usa en el modelo de impresora en lugar de CIEJab porque el modelo de dispositivo debe estar basado únicamente en los datos de colorimétrico disponibles en el DMP. El DMP contiene datos colorimétrico para cada revisión medida, incluido el punto blanco multimedia, por lo que es posible convertir los datos de CIEXYZ en datos de CIELUV. Sin embargo, no es posible convertir a CIECAM02 JCh o jab, ya que no hay acceso a la información de la condición de visualización en el DMP.

### <a name="rgb-projector-device-model-baseline"></a>Línea de base del modelo de dispositivo de proyector RGB

Nota: muchos proyectores de RGB tienen más de un modo de funcionamiento. En un modo, que suele ser el valor predeterminado y se puede llamar algo parecido a "presentación", la respuesta de color del proyector está optimizada para obtener el máximo brillo. Sin embargo, en este modo, el proyector pierde la capacidad de reproducir colores claros, ligeramente cromáticos, como amarillos pálidos y algunos tonos de piel. En otro modo, a menudo denominado "película", "vídeo" o "sRGB", el proyector está optimizado para la reproducción de imágenes realistas y escenas naturales. En este modo, el brillo máximo se renegocia para mejorar la calidad general de la reproducción de color. Para obtener una reproducción de color satisfactoria con proyectores RGB, es necesario colocar el proyector en un modo en el que se pueda reproducir una gama de colores fluida.

![Diagrama que muestra un modelo de dispositivo D L P.](images/cdmp-image167.png)

**Figura 9** : modelo de dispositivo DLP

Un valor RGB entrante pasa por dos rutas de cálculo. El primero es el modelo de matriz, que da como resultado un valor XYZ. Esto va seguido inmediatamente de la conversión de XYZ a Luv. La segunda es la interpolación LUT no uniforme mediante la interpolación tetrahedral. La salida de la interpolación ya está en el espacio Luv por construcción. Las dos salidas se agregan para obtener el valor de Luv predicho. Finalmente, esto se convierte en XYZ, que es la salida esperada del modelo de colorimétrica para el dispositivo DLP.

Dado que los proyectores son dispositivos de pantalla, también admiten la inversion del modelo, es decir, la transformación de XYZ a RGB. Dado que el modelo de dispositivo transforma el espacio RGB en espacio XYZ, que son ambos de tres dimensiones, la inversión es equivalente a la resolución de tres ecuaciones no lineales en tres desconocidos. Esto puede realizarse mediante técnicas de resolución de ecuaciones estándar, como Newton-Raphson. Sin embargo, es preferible convertir primero XYZ en Luv y, a continuación, invertir el Luv en transformación RGB, ya que el espacio Luv es más linealmente lineal que el espacio XYZ.

### <a name="icc-device-model-baseline"></a>Línea de base del modelo de dispositivo ICC

La interoperabilidad de los flujos de trabajo de ICC CITAda se habilita mediante la creación de un perfil de modelo de dispositivo de línea de base de dispositivo ICC especial que almacena el objeto de perfil y crea una transformación ICC mediante un perfil de empresa no operativa. Esta transformación se usa para la conversión entre los colores de dispositivo y CIEXYZ.

![Diagrama que muestra la interoperabilidad de flujo de trabajo c I T E I c i.](images/cdmp-image168.png)

**Figura 10** : interoperabilidad de los flujos de trabajo de ICC

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la administración del color](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





